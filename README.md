# What is this tool exactly ?
This is a tool that functions through editing the Windows Registry, it registers some keys inside certain paths in the current user's hive (which is HKEY_CURRENT_USER)


The point of the tool is to add a certain functionality, as seen in the images posted, that if you right-click a .tex/.dds file, you see a new option in the Context Menu to convert to the other format

Main reason I tried to implement such concept, is that for another game (Spider-Man: Web of Shadows), I made a BlenderToolkit, and then I thought such concept would be easier than using the drag-and-drop functionality I already supported in that tool, to convert between .dds and the game's format for texture files.

Then I decided to expand the idea to RE Engine's DMC5 mainly for the sake of learning and fun. I actually learned a lot from working on this tool about Context Menus/Windows Registry/Hives and much more about the capabilities of Python programming.


The tool has been tested a bit on RE3R_RT and I added the entries myself to the code, if you want to know how to add entries for other games, go to [Is this for DMC5 only](#Is-this-for-DMC5-only) section, but make sure to read other sections too.

# Who can use this tool ?
- It can be useful for modders, who create mods and deal with game files a lot
- It can benefit anyone who might prefer a right-click menu tool to using a batch convert/drag-and-drop tool or even using Blender, for whatever reason.
There could be any number of reasons why anyone might find this tool interesting or useful. At the end of the day, it's up to you if you decide to use it or not.
However, if you ever decide to use it, make sure to read the description and `How To Install.txt` file very well before anything.

# How To Install/Uninstall
To install this tool, simply double-click to run the ~Context_Installer.py~ (assuming Python is registered in your PATH and is associated with .py files as the default app and everything)


### No admin privileges needed



The tool asks for confirmation before every step. If you want to proceed with installation simply type "yes", otherwise type "no"
Before every key being registered or unregistered, the user is asked for confirmation too.
Once installed you should see the menus in the images when right-clicking a .dds file or a .tex file

To uninstall run the script, when it asks first time type "no", and then type yes for whatever key you want to unregister (all of them if you want to remove everything completely)


It will unregister the same paths that were added and for the current user's hive only (HKEY_CURRENT_USER)


For the sake of safety, you can always back-up your current registry before adding anything through several methods. Simplest is exporting the root of the whole registry as a .reg file (Win2k/XP), I exported mine and it is around 300 MB in size.



# Is this for DMC5 only ?
Since the tool is based on and refers to alphaZomega's [RE_Engine_TEX.bt](https://github.com/alphazolam/RE-Engine-010-Templates/blob/main/RE_Engine_TEX.bt) and NSACloud's [RE Mesh Editor](https://github.com/NSACloud/RE-Mesh-Editor)
who already have supported multiple versions in their tools,
I believe my tool could work for other versions of other RE Engine games.
I only have DMC5, so I could only do some tests on this one. The rest is completely untested and there's uncertainity about if this tool can work for them or not.

If you want to extend this tool for other games, open ~Context_Installer.py~ in any code/text editor, and add a new entry like this for instance:
  
`("RE4", ".143221013")`


Also don't forget to add the version extension in ~Convert.py~ at the top, check the images


`"143221013"`


Write the correct version for each game ! Ray Tracing and Non Ray Tracing versions of the same game can have different versions for assets like textures.

Check the images to know which part in the code you add the entries to.

Save changes to the file, run the script again and it should appear.


# Credits & References
- alphaZomega's [RE_Engine_TEX.bt](https://github.com/alphazolam/RE-Engine-010-Templates/blob/main/RE_Engine_TEX.bt)
- NSACloud's [RE Mesh Editor](https://github.com/NSACloud/RE-Mesh-Editor)
- Microsoft's Documentation on [DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dds-header) and [DXGI_FORMAT](https://learn.microsoft.com/en-us/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)
Thanks to everyone who helped do a bit of testing on this tool

In case any issues are encountered, make a post/bug report or contact me on Discord (username: haruse31)
