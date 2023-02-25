# Setup

## Project Creation

There are two types of mods for ULTRAKILL - BepInEx and UMM.  

BepInEx is easier to set up, but UMM supports unloading and reloading, as well as some useful functions like custom keybinds.
We'll be using BepInEx, but it's easy to convert it later.

First, open the Command Prompt, and enter the directory in which you want the project to be made. 
```bat
cd C:\Path\To\Your\Folder
```

Then, run this to create the project.
```bat
dotnet new bepinex5plugin -n <plugin name> -T netstandard2.0 -U 2019.4.16
```  

When done, you should have a folder with the name of your mod where you ran the command. Open it, there should be 3 files `NuGet.Config`,`Plugin.cs` and `<plugin name>.csproj`. Open the `.csproj` file with Visual Studio, or your prefered IDE.
!!! warning
    If you are using Visual Studio Code, doing so will open the file, not the project. Open the directory with VSCode instead.

Once Visual Studio loads, open `Plugin.cs` in the Solution Explorer. This will be the core of your mod, and it should look like this:
```cs linenums="1" title="Default BepInEx Plugin"
using BepInEx; //(1)!

namespace Plugin
{
    [BepInPlugin(PluginInfo.PLUGIN_GUID, PluginInfo.PLUGIN_NAME, PluginInfo.PLUGIN_VERSION)] //(2)!
    public class Plugin : BaseUnityPlugin //(4)!
    {
        private void Awake() //(3)!
        {
            // Plugin startup logic
            Logger.LogInfo($"Plugin {PluginInfo.PLUGIN_GUID} is loaded!");
        }
    }
}
```

1.  This line imports the `BepInEx` namespace, letting us use any code in it - like `BepInPlugin`, or `BaseUnityPlugin`.

2.  This `Attribute` tells BepInEx the metadata of your mod.

3.  The function `Awake()` is the first to be called when the mod is loaded.

4.  BaseUnityPlugin extends from [MonoBehaviour](https://docs.unity3d.com/ScriptReference/MonoBehaviour.html), so you can use functions such as `Update()`, which is called on every frame.

If it doesn't look like this, you messed something up. Congratulations! V1 is rapidly approaching your house, and assuming you can't slide and dash, he's probably faster than you. Good luck!

## Adding Libraries

Considering you're making a mod, you probably want to change stuff. For that, we need to add the game's code first.

Begin by opening your ULTRAKILL folder. If you don't know how to do that, open Steam, and do this.

![open steam path](https://cdn.discordapp.com/attachments/727956051156271175/1079171277388005456/image.png)

From there, navigate to `ULTRAKILL_Data\Managed`, and you'll see a lot of DLL files. Copy down this path, because you'll need it.

Then, back in Visual Studio, right-click on the Dependencies button in the Solution Explorer, and press Add Project References, then Browse.

![references image](https://media.discordapp.net/attachments/727956051156271175/1079183475258703924/image.png)

Navigate to the path you copied down, then add `Assembly-CSharp.dll`, as well as every one starting with `UnityEngine`. This will add all of the code from ULTRAKILL and Unity, letting us use it for the mod.

This may take a while to load, so grab a snack.

## Building

Now we've got our basic set-up out the way, we need to make sure that it works.

Press `Ctrl + B` to build, and you should see some output at the bottom of your screen.

!!! warning
    You might get an error like `'PluginInfo' does not contain a definition for 'PLUGIN_GUID'`. 
    
    In this case, replace both instances of `PluginInfo.PLUGIN_GUID` with your own GUID (we suggest `yourname.ultrakill.modname`), `PluginInfo.PLUGIN_NAME` with your mod's name, and `PluginInfo.PLUGIN_VERSION` with the mod's [semver](https://devhints.io/semver) version - start with `1.0.0`.

Among other things, you should see `<project name> -> "C:\Path\To\Your\Folder\bin\Debug\netstandard2.0\<plugin name>.dll` - this is the folder the mod has been built to.

![build success](https://media.discordapp.net/attachments/727956051156271175/1079179511926640660/image.png)

Go to said folder, and you'll see a few DLLs.

![folder with dlls](https://media.discordapp.net/attachments/727956051156271175/1079180682804342894/image.png)

Copy the one with your mod's name, and paste it into `ULTRAKILL\BepInEx\plugins`. Afterwards, run the game, and close it again.

Then, navigate to `ULTRAKILL\BepInEx\`, and open `LogOutput.log`. 

![log in folder](https://media.discordapp.net/attachments/727956051156271175/1079181031061602384/image.png)

With any luck, you should see a line that reads `Plugin <plugin name> is loaded!`.

![log from mod](https://media.discordapp.net/attachments/727956051156271175/1079180304100626472/image.png)

If you do, well done! You have a functional mod.