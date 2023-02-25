# Where do I start

There are two types of mods for Ultrakill. BepInEx and UMM.  
We'll explain the differences later but for now, we'll be using BepInEx. Switching later should be easy as breathing if you understand the basics.  

To start, create a new BepInEx project using this command  

```bat
dotnet new bepinex5plugin -n <plugin name> -T netstandard2.0 -U 2019.4.16
```  
or the convenient batch script I made (if you're on Windows) 
```bat
@echo off
set /p name=Mod name: 
dotnet new bepinex5plugin -n %name% -T netstandard2.0 -U 2019.4.16
```  

When done, you should have a folder with the name of your mod where you ran the command. Open it, there should be 3 files `NuGet.Config`,`Plugin.cs` and `<plugin name>.csproj`. Open the `.csproj` file with Visual Studio (or your prefered IDE)
!!! warning
    If you are using Visual Studio Code, doing so will open the file, not the project. Open the directory with VSCode instead.

Once Visual Studio finishes loading, select `Plugin.cs` in the Solution explorer adn you should see something like this 
```cs linenums="1"
using BepInEx;

namespace Plugin
{
    [BepInPlugin(PluginInfo.PLUGIN_GUID, PluginInfo.PLUGIN_NAME, PluginInfo.PLUGIN_VERSION)]
    public class Plugin : BaseUnityPlugin
    {
        private void Awake()
        {
            // Plugin startup logic
            Logger.LogInfo($"Plugin {PluginInfo.PLUGIN_GUID} is loaded!");
        }
    }
}
```
