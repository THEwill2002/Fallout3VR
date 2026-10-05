# Controller controls — alpha 0.1.0-alpha.1

Quest controller labels are used below. Both controllers must be awake and tracked. Controls are contextual.

| In game | Action |
| --- | --- |
| Left stick | Move, relative to head direction |
| Right stick left/right | Turn |
| Right trigger | Fire / native attack |
| A | Interact with the object targeted by gaze |
| X | Reload / ready item through the game's binding |
| Y | Open Pip-Boy |
| B | Jump |
| Hold right grip, then press B | Pause / native Escape; repeat to return |
| Hold both grips for one second | Recenter |
| Left grip near a supported weapon | Attach support hand; hold to keep the grip |

Hand tracking starts automatically. Releasing the left grip detaches it. Moving the support hand too far away also detaches it; release the grip before trying again.

## Pip-Boy and menus

| Input | Action |
| --- | --- |
| Left stick | Navigate lists and subcategories |
| Right stick | Move mouse cursor |
| A / right trigger | Confirm |
| X in Pip-Boy | Cycle Stats / Items / Data |
| Y | Contextual back / close |
| Left trigger in Pip-Boy | Mouse click; hold and move right stick to drag the map from an empty area |
| Left grip + left stick up/down | Map zoom in 0.64 using Page Up / Page Down; return stick to centre first |
| Right grip + B | Native Escape / back |

Zoom was confirmed working by the development tester on October 1, 2026. It is only routed while Pip-Boy is detected; outside its map, the same keys may navigate the current native page.

## Keyboard fallbacks

- F6: VR tracking on/off.
- F10: recenter.
- Ctrl+T: switch smooth / snap turning.
- Ctrl+U: show/hide the gameplay HUD.
- Ctrl+J: toggle tracked weapon control; it is already enabled automatically.
- Ctrl+B: enable/disable two-handed grip for the currently recognized weapon mesh; remembered per mesh.
- Ctrl+End: close the VR scene.

F8 diagnostics are for local development. Do not publish the resulting game mesh captures.


- Ctrl+Shift+R: compare SteamVR rotational reprojection (on by default in SteamVR).
- Ctrl+Alt+W: compare stable water material reflection with native planar reflection.
- Ctrl+Alt+H: two-step left-hand orientation calibration: first hold the real controller in the desired neutral pose and press, then rotate until the virtual hand looks correct and press again. Ctrl+Alt+Shift+H resets this user calibration.

The launcher enables VR automatically. F6 remains a manual toggle. New-user calibration and free-hand mesh pose may differ from the development videos; no extracted pose data is shipped.

