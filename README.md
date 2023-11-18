# 1. Intro

This guide will cover one example of installing the tools required to start with MG modding. This will show the installation process starting with a fresh install of Windows 11, adding all the required programs, tools, templates, and all of the other required dependencies. 
This guide was authored by someone who had recently gone through the process of setting up an environment for modding, and is NOT an expert at any of these applications. The steps here are just what worked for them. Main resource used when creating this documentation was the modding documentation provided by Fede [https://docs.fedes.uy/](https://docs.fedes.uy/)

Also, before we begin, just make sure that you have enough free disk space. A rough estimate on disk space required for all the tools is ~30GB. More space will be required for the Unity projects, 3D models, textures, Visual Studio projects, etc. 

# 2. Unity

Unity is the game engine that My Garage was developed for. Any mods that add 3d models, sounds, new game objects, or modify/copy existing game objects will likely require the use of Unity. It is highly recommended to use the version that game uses (2020.3.0.f1.

 * Official Unity documentation: [https://docs.unity3d.com](https://docs.unity3d.com)
 * Unity installation documentation: [https://docs.unity3d.com/Manual/GettingStartedInstallingUnity.html](https://docs.unity3d.com/Manual/GettingStartedInstallingUnity.html)

## 2.1 Installing Unity Hub

These steps will only cover the process of installing Unity using Unity Hub, as you will require Unity Hub anyways. This will assume that you already have a Unity account, but have not installed Unity Hub yet. The install is straight forward, and should only take a minute.

1. Download Unity Hub from the main Unity website: [https://unity.com/download](https://unity.com/download)
2. When the download is complete, run the installer
3. Depending on your Windows configuration, you will likely get this prompt, click "Yes"
 * ![Image showing Windows User Account Control Dialog](/mgmoddocs/images/environment/UnityHub01.png)
4. Accept the license terms
 * ![Image showing the Unity Hub License Agreement step in the installer](/mgmoddocs/images/environment/UnityHub02.png)
5. Change the installation path if you want to, and then click Install
 * ![Image showing the Unity Hub Choose Install Location step in the installer](/mgmoddocs/images/environment/UnityHub03.png)
6. The Unity installation will take a few seconds
 * ![Image showing the Unith Hub installer, with a progress bar](/mgmoddocs/images/environment/UnityHub04.png)
7. Once the installation is complete, leave the "Run Unity Hub" checked, and click the Finish button.
 * ![Image showing the Completed Unity Hub setup dialog](/mgmoddocs/images/environment/UnityHub05.png)

## 2.2 Running Unity Hub for the first time

Next, we will need to set up Unity Hub so that we can download and use the Editor. We basically need to Add a license to be able to use Unity.

1. When Unity Hub launches, click the Sign In button, or create an account if you haven't already.
 * ![](/mgmoddocs/images/environment/UnityHub06.png)
2. This should open your default web browser to the Unity website where you can log in. Enter your info and click Sign In
 * ![](/mgmoddocs/images/environment/UnityHub07.png)
3. You might be prompted with this alert in your browser, select "Always allow" and then click Open Link
 * ![](/mgmoddocs/images/environment/UnityHub08.png)
4. Unity Hub should now show that it is signing you in:
 * ![](/mgmoddocs/images/environment/UnityHub09.png)
5. Unity Hub will prompt asking you to install the latest version of the Unity Editor, click the "Skip installation" button in the bottom
 * ![](/mgmoddocs/images/environment/UnityHub10.png)
6. You will likely have a banner along the top of Unity Hub prompting you to activate your license, click the Manage Licenses button
 * ![](/mgmoddocs/images/environment/UnityHub11.png)
7. Click the Add license button
 * ![](/mgmoddocs/images/environment/UnityHub12.png)
8. Click "Get a free personal license" if you don't have subscription already
 * ![](/mgmoddocs/images/environment/UnityHub13.png)
9. Review the terms, and if you agree, click the button to agree
 * ![](/mgmoddocs/images/environment/UnityHub14.png)
10. It should now add the personal license to the list of available licenses. Close the licenses dialog
11. We are now ready to install the Unity Editor

## 2.3 Installing Unity Editor

To make mods for My Garage, we now need to install the same version of the Unity Editor as is used to build the game. This ensures that the Unity Engine libraries we use are the same as the game for compatibility.

1. Open Fede's download page [https://docs.fedes.uy/#/downloads](https://docs.fedes.uy/#/downloads)
2. In the Unity section, click the Unity Hub link
3. Your browser might prompt you with this message, click the Open Link button
 * ![](/mgmoddocs/images/environment/UnityEditor01.png)
4. Unity Hub should display the following module selection screen. Unselect the Visual Studio Community 2019 and click Install. We don't need VS 2019, and will install a newer version later.
 * ![](/mgmoddocs/images/environment/UnityEditor02.png)
5. You will likely now have a Downloads dialog open in Unity Hub, showing the progress of the install, this is a big download and can take a while depending on your connection speed. If you close this dialog, you can reopen it by clicking the Downloads button in the bottom left of the Unity Hub to view the progress.
 * ![](/mgmoddocs/images/environment/UnityEditor03.png)
6. When the download is complete, you will likely get this prompt, click "Yes" to start the install
 * ![](/mgmoddocs/images/environment/UnityEditor04.png)
7. The install process will be just waiting for the progress bar some more, though this should be fairly quick.
 * ![](/mgmoddocs/images/environment/UnityEditor05.png)
8. Wait until the install is complete, and then close the downloads dialog
 * ![](/mgmoddocs/images/environment/UnityEditor06.png)
9. It should now show the 2020.3.0f1 version of Unity Editor in the installs section of Unity Hub
 * ![](/mgmoddocs/images/environment/UnityEditor07.png)

# 3. Visual Studio 2022

Visual studio is the development environment used to create the scripts/code that ties everything together, and compiles the final mod dll files that the game/ModUtils can load. FedesUy has provided a Visual Studio project template to make it easy to get started, that helps with some of the basic project setup.

Official documentation is available here: [https://learn.microsoft.com/en-us/visualstudio/install/install-visual-studio?view=vs-2022](https://learn.microsoft.com/en-us/visualstudio/install/install-visual-studio?view=vs-2022)

## 3.1 Installing Visual Studio 2022

1. Download the Community edition of Visual studio 2022: [https://visualstudio.microsoft.com/downloads/](https://visualstudio.microsoft.com/downloads/)
2. When the download is complete, run the VisualStudioSetup.exe
3. You will likely be prompted with this, click Yes
 * ![](/mgmoddocs/images/environment/VisualStudio01.png)
4. Review the privacy policy and the license terms, and then click continue:
 * ![](/mgmoddocs/images/environment/VisualStudio02.png)
5. It will download some basic installer components, should be pretty quick
 * ![](/mgmoddocs/images/environment/VisualStudio03.png)
6. You should then be prompted to select what "Workloads" to install. For modding My Garage, and Unity Games in general, we will need the .NET desktop development. Select it.
 * ![](/mgmoddocs/images/environment/VisualStudio04.png)
7. This should display components in the right side. We won't need all of them, and can unselect a few of them to save some space, this is the component set that I chose to install
 * ![](/mgmoddocs/images/environment/VisualStudio05.png)
8. After selecting the components, click the Install button in the bottom right:
 * ![](/mgmoddocs/images/environment/VisualStudio06.png)
9. You should now see some progress bars showing the status of the installation. This can take a while.
 * ![](/mgmoddocs/images/environment/VisualStudio07.png)
10. When the installation is complete, you will likely be prompted to sign in, just click "Skip this for now"
 * ![](/mgmoddocs/images/environment/VisualStudio08.png)
11. Pick a color theme, and then click Start Visual Studio
 * ![](/mgmoddocs/images/environment/VisualStudio09.png)
12. At the next screen to open or create a project, just close Visual studio for now.

# 4. Blender

Blender is free software that is used for 3D modeling, among other things. You can use it to design 3d models for new cars, parts, tools etc to be used in game. The installation for this is pretty straight forward.

Official installation documentation is available here: [https://docs.blender.org/manual/en/4.0/getting_started/installing/index.html](https://docs.blender.org/manual/en/4.0/getting_started/installing/index.html)  Links are at the bottom of that page to instructions for different operating systems. The below steps are just what I went with.

## 4.1 Blender Installation

1. Download the latest version of Blender from the official website [https://www.blender.org/download/](https://www.blender.org/download/)
2. When the download is complete, run the installer.
3. As of the writing of this guide, Blender 4.0.1 was just released, and Windows will likely prompt with this scary looking dialog due to the installer not being run on all that many systems yet:
 * ![](/mgmoddocs/images/environment/Blender01.png)
4. Click the "More Info" to review the App, and Publisher, if it looks like the following, click "Run anyway"
 * ![](/mgmoddocs/images/environment/Blender02.png)
5. The install is straight forward from here. Click next
 * ![](/mgmoddocs/images/environment/Blender03.png)
6. Review and accept the terms, and then click next
 * ![](/mgmoddocs/images/environment/Blender04.png)
7. Leave the default components in the custom setup, just click Next
 * ![](/mgmoddocs/images/environment/Blender06.png)
8. Click Install
 * ![](/mgmoddocs/images/environment/Blender07.png)
9. During the install, you may be prompted with this dialog, click "Yes"
 * ![](/mgmoddocs/images/environment/Blender08.png)
10. Eventually, blender will finish install, click Finish
 * ![](/mgmoddocs/images/environment/Blender09.png)
	
# 5. dnSpy

Official repo: [https://github.com/dnSpy/dnSpy](https://github.com/dnSpy/dnSpy)

dnSpy is a tool that lets you peak at the intermediate language code for some applications. Intermediate Language code, or IL Code for short, is a partially compiled version of the code for an application, that can be re-interpreted back into a human readable form using some tools like dnSpy. This will allow you to take a look at some of the dll files for the core game, the mod utilities, and also other mods. This is very useful for gaining an understanding of how the core game mechanics work, and allows you to see how other mods work to help with developing your own mods. dnSpy can be used also to modify and recompile existing dlls to change their functionality, adding debug logging as an example. One thing to note about the code displayed in dnSpy, is that since it is partially compiled, the code flow can vary quite a bit from the original source code.

There are several alternate applications that have similar functionality, though they won't be covered in this guide. ILSpy and dotPeek are two of the more common alternatives.

**CAUTION: There have been some releases of dnSpy that were bundled with malware, that were uploaded to various websites a few years ago. Only download dnSpy from the official Github repository!**

## 5.1 Installing dnSpy

1. Open the official github repo [https://github.com/dnSpy/dnSpy/releases/tag/v6.1.8](https://github.com/dnSpy/dnSpy/releases/tag/v6.1.8)
2. Download either the netframework or x64 version of dnSpy
3. Extract the archive to a folder where you would like to "install" it to
4. Example showing extracted files from netframework package
 * ![](/mgmoddocs/images/environment/dnSpy01.png)

# 6. Unity Explorer

Unity Explorer is a tool that can be used to inspect, and interact with game objects and components within a Unity game while the game is running. This is useful for understanding how the core game works, debugging issues with mods, and more.

**NOTE: Using Unity Explorer in My Garage can interfere with your ability to interact with some in game menus! If you can't interact with a menu while using Unity Explorer, try pressing F7 and then interact with the game menu.**

Unity Explorer requires something to inject it into the game at runtime like BepInEx or MelonLoader. This guide currently only has steps for BepInEx, though the documentation for MelonLoader is very detailed and process should be pretty similar.

 * Unity Explorer repository: [https://github.com/sinai-dev/UnityExplorer](https://github.com/sinai-dev/UnityExplorer)
 * MelonLoader repository: [https://github.com/LavaGang/MelonLoader](https://github.com/LavaGang/MelonLoader)
 * BepInEx repository: [https://github.com/BepInEx/BepInEx](https://github.com/BepInEx/BepInEx)

## Unity Explorer Installation 

1. Download the latest x64 release of BepInEx [https://github.com/BepInEx/BepInEx/releases](https://github.com/BepInEx/BepInEx/releases) version 5.4.22 was the latest at the time of this guide being written.
2. Open Steam, find My Garage in the games list
3. Right click on the game > Manage > Browse local files
 * ![](/mgmoddocs/images/environment/UnityExplorer01.png)
4. It should open the game install directory
 * ![](/mgmoddocs/images/environment/UnityExplorer02.png)
5. Open the BepInEx zip file, and extract the contents to the game install directory
 * ![](/mgmoddocs/images/environment/UnityExplorer03.png)
6. Open the BepInEx directory, leave this folder open for the time being.
7. Go to the latest release page for Unity Explorer [https://github.com/sinai-dev/UnityExplorer/releases](https://github.com/sinai-dev/UnityExplorer/releases)
8. You must download a specific version of Unity Explorer that is compatible with the version of BepInEx we are using. Find the most recent version with a download for UnityExplorer.BepInEx5.Mono.zip, as of this guide, the latest was 4.9.0
9. Open the downloaded zip file, and copy the "plugins" folder into the BepInEx folder
 * ![](/mgmoddocs/images/environment/UnityExplorer04.png)
10. Start My Garage and wait for the main menu to load, if you see a new toolbar along the top, it is working
