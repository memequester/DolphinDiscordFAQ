# DolphinDiscordFAQ
```
Running Dolphin
```
**What CPU/GPU do I need for Dolphin?**
Minimum requirements:
-   **OS:** 64-bit edition of Windows (7 SP1 or higher), Linux, or macOS (10.12 Sierra or higher). Windows Vista SP2 and unix-like systems other than Linux are not officially supported but might work.
-   **CPU:** A CPU with SSE2 support. A modern CPU (3 GHz and Dual Core, not older than 2008) is highly recommended.
-   **Graphics:** A reasonably modern graphics card (Direct3D 10.0 / OpenGL 3.0). A graphics card that supports Direct3D 11 / OpenGL 4.4 / Vulkan 1.1 is recommended. Ensure that your drivers are up to date. 

**Why is my version of Dolphin missing features?** 
You may be using an outdated version of Dolphin. Update to the latest beta or dev version here: https://dolphin-emu.org/download and install the latest C++ redist: https://aka.ms/vs/17/release/vc_redist.x64.exe

```
Compatibility
```
**Does Wiimmfi work?**

Yes, but some games will require a real NAND backup from your Wii and your Wii's MAC Address. vWii NANDs from a Wii U *may* work. NANDs generated with third-party tools do  *not* work for many games. Check the patching and configuration instructions for your game.

**Does Riivolution work?** 

As of version 5.0-15407, Dolphin supports Riivolution patches. Extract and move your patches to `[your user documents folder]\Dolphin Emulator\Load\Riivolution`. In Dolphin, right-click on your game in the game list and click `Start with Riivolution Patches...`.
󠀀󠀀󠀀󠀀
```
Controllers
```
**Where do I find the directory for controller configurations?** 

`[your user documents folder]/Dolphin Emulator/Config/Profiles/Wiimote` _or_ `[your user documents folder]/Dolphin Emulator/Config/Profiles/GCPad`

**How do I stop emulated Wii remote not being able to reach the edges of my screen?** 

The Wii remote must be configured (emulated controls of course) to use the whole screen space in Dolphin. To change the screen space, change the Total Yaw and Total Pitch in the controller settings for the emulated Wii remote(s).

**Can I use a real Wii remote?**

Wii remotes connect with Bluetooth, so you'll need a Bluetooth adapter. For pointer functionality, you'll either need a sensor bar (official, third-party or makeshift) or you'll need to set up pointer emulation. Use `!wiimote` in #bot-commands for full setup instructions. 

**Do I need a Dolphinbar?**

The Dolphinbar is not a requirement for Dolphin. However, for users with no existing bluetooth adapter, the Dolphinbar is a convenient Bluetooth adapter + sensor bar combo.

**Can I use Joycon / Switch Procon / Dualshock / Dualsense controllers?**

Middleware programs such as DS4windows and BetterJoy allow these controllers to be used with Dolphin. These programs can also make use of the DSU protocol to allow the motion sensors in these controllers to be mapped to an emulated Wii remote. Refer to https://wiki.dolphin-emu.org/index.php?title=DSU_Client for more advice.

```
Netplay
```
**How do I set up Netplay?**

https://dolphin-emu.org/docs/guides/netplay-guide/
TL;DR: Use the latest beta version, use identical dumps, use the traversal server to avoid portforwarding, and carefully read the Controller and Netplay Settings sections of the guide.

**Where can I find users to Netplay with?**

Use `Tools` > `Browse Netplay Sessions...` to browse Netplay sessions on the transversal server. You can also check #multiplayer or look around for dedicated multiplayer Discord servers for your game.

```
Contributing to Dolphin
```
**What should I do if I've found a bug?**

First, check that it's not caused by something else. Verify your game files and disable any cheats or patches.
If the issue persists, check if it has already been reported on our Issue Tracker: https://bugs.dolphin-emu.org/projects/emulator/issues
If it hasn't been reported, create a new report. Follow the template provided on the issue tracker.

**How do I contribute code to Dolphin?**

Open a pull request with your changes here: https://github.com/dolphin-emu/dolphin/compare. New contributors are not auto-trusted, so your PR must be reviewed by a trusted contributor before further action is taken. 

```
Customisation
```
**Where can I find User Styles? How do I enable one?**

Styles are advertised on this Dolphin forum thread: https://forums.dolphin-emu.org/Thread-user-style-thread. Place style files in `[your user documents folder]/Dolphin Emulator/User/Styles`. To switch to a user style, navigate to `Config` > `Interface`, tick `Use Custom User Style`, and select the style with the `User Style` dropdown.

**How do you edit settings on a per-game basis?**
To edit per-game settings Dolphin uses `.ini` files. 
1) Right-click your game in Dolphin and click through `Properties` > `Editor` tab.
2) In the `Presets` dropdown, click `Editor` > `Open in External Editor`. 
3) Refer to https://wiki.dolphin-emu.org/index.php?title=GameINI for a list of config flags.

**How do I change a game's name?**
1) Create a `titles.txt` file in `[your user documents folder]\Dolphin Emulator\Load`. 
2) Find the Game ID of your game. This 6 character code can be found in the window titlebar when running the game, or in the titlebar of the game's `Properties` window.
3) Add the game ID and its new name into the text file as shown in the example below: 
	`GALE01 = Super Smash Bros. Melee` 
	`GF7E01 = Star Fox: Assault`
4) Save the `.txt` file and relaunch Dolphin.

**How do I change a game's banner?**
1) Create your banner in whatever program you'd like. Make sure the aspect ratio of the image is 3:1 width:height (e.g. 96x32, 288x96).
2) Save the banner as a `.png` file with the naming format `[iso name].png`. For example, the banner for `Super Mario Sunshine.iso` would be named `Super Mario Sunshine.png` 
3) Place the `.png` file in the same directory as the matching `.iso` file.

**How do I change a game's cover art?**
1) Create your cover in whatever program you'd like. Make sure the aspect ratio of the image is 5:7 width:height (e.g. 160x224, 640x896).
2) Save the cover as a `.png` file with the naming format `[iso name].cover.png`. For example, the cover for `Super Mario Sunshine.iso` would be named `Super Mario Sunshine.cover.png` 
3) Place the `.png` file in the same directory as the matching `.iso` file.
