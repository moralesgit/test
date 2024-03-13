# GraphicsAPI
Made this tool for [Diversity](https://thunderstore.io/c/lethal-company/p/IntegrityChaos/Diversity/).

## Graphic Settings (EXPERIMENTAL)
### Usage:
- Add the following namespaces:
```c#
using GraphicsAPI;
using UnityEngine.Rendering.HighDefinition;
using UnityEngine.Rendering;
using static UnityEngine.Rendering.HighDefinition.RenderPipelineSettings;
```
- Fetch the current HDRP Render Pipeline Settings with the following:
```c#
RenderPipelineSettings settings = HDRPGraphicSettings.GetCurrentSettings();
```
- Then make changes to the settings:
```c#
settings.customBufferFormat = CustomBufferFormat.R11G11B10;
```
- Finally apply the new settings:
```c#
HDRPGraphicSettings.ApplySettings(settings);
```
### Full example:
```c#
using GraphicsAPI;
using HarmonyLib;
using UnityEngine.Rendering.HighDefinition;
using UnityEngine.Rendering;
using static UnityEngine.Rendering.HighDefinition.RenderPipelineSettings;
using UnityEngine;

namespace SuperAwesomeMod.Patches
{
    [HarmonyPatch(typeof(PreInitSceneScript))]
    public class PreInitPatch
    {
        [HarmonyPatch(typeof(PreInitSceneScript), "Awake")] // This patch happens as soon the game opens.
        [HarmonyPrefix]
        static void Awake()
        {
            RenderPipelineSettings settings = HDRPGraphicSettings.GetCurrentSettings();

            settings.customBufferFormat = CustomBufferFormat.R11G11B10;

            HDRPGraphicSettings.ApplySettings(settings);
        }
    }
}
```
## CustomPostProcessing
### Usage:
- Create A full screen shader and apply it to a material for later use. Note: We're back at using the custom color buffer. Please use it in your shaders from now on!
- In your script make sure to include `GraphicsAPI.CustomPostProcessing` and Unity's rendering namespaces!

```c#
using UnityEngine.Rendering.HighDefinition;
using UnityEngine.Rendering;
using GraphicsAPI.CustomPostProcessing;
```
### Create a new `PostProcess`
- Create a new `PostProcess` and give it a name and assign your previously created material. A `PostProcess` will define and set up both "Custom Pass Volume" and the "Full Screen Pass".

```c#
PostProcess myNewPass = new PostProcess("PassName", material);
```

Note: You can't have 2 `PostProcess` of the same name!
### Apply the new `PostProcess`
- Simply add the newly created `PostProcess` into the `CustomPostProcessingManager`!

```c#
CustomPostProcessingManager.Instance.AddPostProcess(myNewPass);
```

Note: This method returns a `FullScreenCustomPass`.
### Enable / Disable
- If you wish to enable or disable a pass you can simply use ``.EnablePass(pass);`` or ``.DisablePass(pass);`` to do so!
```c#
CustomPostProcessingManager.Instance.EnablePass(myPass);
```
- Or you can get a pass from its name:
```c#
FullScreenCustomPass myPass = CustomPostProcessingManager.Instance.GetPass("MyPass");

CustomPostProcessingManager.Instance.EnablePass(myPass);
```
## Example 1:
```c#
using UnityEngine;
using UnityEngine.Rendering.HighDefinition;
using UnityEngine.Rendering;
using System.Collections;
using GraphicsAPI.CustomPostProcessing;
using GameNetcodeStuff;

namespace SuperAwesomeMod
{
    public class AddPostProcessing : MonoBehaviour
    {
        private FullScreenCustomPass vignetteFSPass;

        public PlayerControllerB player;

        public Material myFullscreenMaterial;

        void Start()
        {
            // Creating the PostProcess.

            PostProcess vignettePass = new PostProcess("VignettePass", myFullscreenMaterial)
            {
                InjectionType = InjectionType.AfterPostProcess, // You can predefine the PostProcess on creation.
                Enabled = false // Disabling it on creation for example.
            };

            // Adding the PostProcess and assigning it to 'vignetteFSPass'.

            vignetteFSPass = CustomPostProcessingManager.Instance.AddPostProcess(vignettePass);

            // Note that you can't 'remove' a pass. You can simply disable it.
        }

        void Update()
        {
            // Simple if statement to enable/disable the pass according to the dead value of the player.

            if (player.isPlayerDead && vignetteFSPass.enabled)
            {
                vignetteFSPass.enabled = false;
            }
            else if (!vignetteFSPass.enabled)
            {
                vignetteFSPass.enabled = true;
            }
        }
    }
}
```
## Example 2:
```c#
using UnityEngine;
using UnityEngine.Rendering.HighDefinition;
using UnityEngine.Rendering;
using System.Collections;
using GraphicsAPI.CustomPostProcessing;
using GameNetcodeStuff;
using BepInEx;

namespace SuperAwesomeMod
{
    [BepInPlugin(modGUID, modName, modVersion)]
    public class Plugin : BaseUnityPlugin
    {
        public const string modGUID = "Chaos.SuperAwesomeMod";
        public const string modName = "SuperAwesomeMod";
        public const string modVersion = "1.0.0";

        public FullScreenCustomPass myFsPass;

        public PlayerControllerB player;

        void Awake()
        {
            // Subscribing to the OnLoad event.

            CustomPostProcessingManager.OnLoad += OnLoad;
        }

        private void OnLoad(object sender, System.EventArgs e)
        {
            // The sender will always be 'CustomPostProcessingManager'.

            CustomPostProcessingManager manager = (CustomPostProcessingManager)sender;

            Material myFullscreenMaterial = manager.dither; // Using a premade fullscreen material that comes with the API.

            PostProcess myPostProcess = new PostProcess("MyFsPass", myFullscreenMaterial)
            {
                InjectionType = InjectionType.AfterPostProcess // You can predefine the PostProcess on creation.
            };

            // Adding the PostProcess and assigning it to 'myFsPass'.

            myFsPass = CustomPostProcessingManager.Instance.AddPostProcess(myPostProcess);
        }
    }
}
```