# Fallout3VR

**Return to the Capital Wasteland in virtual reality.**

An experimental PC VR mod for Fallout 3, with 6DoF head tracking, tracked controllers, controller locomotion, and a desktop mirror for recording.

**Status: first playable alpha candidate packaged. The GitHub release draft is awaiting final validation of the new launcher; no public binary download yet.**

[Guide français](docs/GUIDE-FR.md) · [Controls](docs/CONTROLS.md) · [Testing and bug reports](CONTRIBUTING.md)

## What works today

- Position and orientation tracking for the headset.
- Tracked weapon movement and an independent left hand on supported meshes.
- Controller movement, interaction, reloading, jumping, and pause.
- Smooth turning, set to 90°/s by default, or snap turning.
- Pip-Boy and menus displayed on a floating panel.
- Controller cursor movement and map dragging.
- A desktop mirror for capturing gameplay.
- Three rendering profiles, including an experimental UHD profile.

These features have been tested during development on one setup. Compatibility with other hardware, game editions, mods, and runtimes is not established.

## Experimental features

| Feature | Current scope |
| --- | --- |
| Two-handed grip | BB gun enabled by default; Ctrl+B remembers opt-in for each recognized weapon mesh. Compatibility varies. |
| Physical melee gestures | Police baton swings trigger a native game attack. This is not full weapon-to-enemy collision simulation. |
| Pip-Boy map zoom | Confirmed working by the development tester in build 0.64. |
| Independent arms | Works on recognized meshes; other outfits and weapons need testing. |
| UHD | 1536 × 1536 transport image per eye; unrestricted physical head orientation. Performance varies. |

## Tested setup

- Fallout 3 on Steam, exact executable build 1.7.0.4 used by the prototype.
- Windows PC with an NVIDIA RTX 4070.
- Meta Quest 3 using Virtual Desktop and SteamVR/OpenXR. The SteamVR correction was confirmed by the development tester.
- The development installation requires the Intel graphics compatibility patch. The mod preserves the existing d3d9.dll and does not distribute that patch.

Quest Link, other headsets, other GPUs, and other Fallout 3 executable versions are not yet confirmed. A supported OpenXR runtime and a legally acquired copy of Fallout 3 are required.

## Before the public alpha

### Optional Intel compatibility patch

If your base game needs the Intel workaround, use the original [Intel HD graphics Bypass package by Bren712 on Nexus Mods](https://www.nexusmods.com/fallout3/mods/17209) and follow its included instructions. This is not a requirement for every PC. Confirm Fallout 3 works without VR first, and keep an existing working `d3d9.dll`. Fallout3VR preserves that file; the patch is not bundled or installed automatically.

The new portable **THEwill_Fallout3_VR.exe** detects Steam libraries and Virtual Desktop/SteamVR, then launches Fallout3.exe directly in VR without the Bethesda Start/Settings window. Extract the entire release ZIP; do not copy only the EXE. HD is the default, with Normal/UHD and runtime overrides in settings.json.

Temporary loader DLLs and display preferences are backed up and restored after closing the game; crash recovery and DLL conflict protection are included. Fixture tests, extracted-package detection checks and six native test suites pass. The new complete launch/quit flow in a headset and a clean second-PC test remain unverified.

## Important limitations

- The renderer alternates eyes across frames; it does not render both eyes synchronously every frame.
- Locomotion currently uses eight-direction keyboard input, not true analog speed.
- Two-handed support and gesture attacks are not enabled for every weapon.
- Tracking a controller is not finger tracking. Arm and hand appearance depends on supported game meshes.
- There is no native VR Settings page in Fallout's menu yet.
- Automated tests check math, input routing, and state transitions. They do not prove visual correctness or a stable headset frame rate.

## Next priorities

- Improve controller-only menu navigation.
- Expand reliable weapon identification for two-handed grip and melee gestures.
- Test more outfits, interiors, and long sessions.
- Validate the new portable launcher on a second PC.
- Prepare a reproducible public source/build package if the project source is released.

## Feedback

Use [GitHub Issues](https://github.com/THEwill2002/Fallout3VR/issues/new/choose): choose **Bug report** for a problem or **Alpha feedback** for compatibility results and suggestions. French and English are welcome. Successful tests on other setups are useful too. The forms are ready ahead of the public download; see [the reporting guide](CONTRIBUTING.md).

Do not upload game assets, saves, diagnostic mesh captures, or an unreviewed copy of your logs.

## Project and third-party licensing

The initial candidate contains playable binaries and launcher scripts. A project source-code license has not been selected. Binary use permission and third-party notices are included in the package; no open-source status is claimed.

This is an unofficial fan project, not affiliated with or endorsed by Bethesda or Meta. Fallout game files are not included.
