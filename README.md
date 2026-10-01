# Fallout3VR

**Return to the Capital Wasteland in virtual reality.**

An experimental PC VR mod for Fallout 3, with 6DoF head tracking, tracked controllers, controller locomotion, and a desktop mirror for recording.

**Status: private pre-alpha testing. A public alpha is being prepared; no public download is available yet.**

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
| Two-handed grip | BB gun support; other weapons require the experimental universal mode. |
| Physical melee gestures | Police baton swings trigger a native game attack. This is not full weapon-to-enemy collision simulation. |
| Pip-Boy map zoom | Confirmed working by the development tester in build 0.64. |
| Independent arms | Works on recognized meshes; other outfits and weapons need testing. |
| UHD | 1536 × 1536 transport image per eye; unrestricted physical head orientation. Performance varies. |

## Tested setup

- Fallout 3 on Steam, exact executable build 1.7.0.4 used by the prototype.
- Windows PC with an NVIDIA RTX 4070.
- Meta Quest 3 using Virtual Desktop and OpenXR.
- The development installation requires the Intel graphics compatibility patch. The mod preserves the existing d3d9.dll and does not distribute that patch.

Quest Link, other headsets, other GPUs, and other Fallout 3 executable versions are not yet confirmed. A supported OpenXR runtime and a legally acquired copy of Fallout 3 are required.

## Before the public alpha

The current development launchers still contain machine-specific paths. They are not a general-purpose installer yet. Do not copy the development workspace into your game folder.

The public package needs portable installation and restoration, a dependency and licensing review, and a clean-install test on another PC before release. Public installation instructions and downloads will be added when that package is ready.

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
- Prepare a portable installer and a reproducible public source/build package.

## Feedback

When public testing opens, please report one problem per issue with your game version, headset, runtime, rendering profile, and reproduction steps. See [the reporting guide](CONTRIBUTING.md).

Do not upload game assets, saves, diagnostic mesh captures, or an unreviewed copy of your logs.

## Project and third-party licensing

The project code license is still being selected. No license grant for the project code is asserted by this preview. Third-party components retain their own licenses and notices.

This is an unofficial fan project, not affiliated with or endorsed by Bethesda or Meta. Fallout game files are not included.

