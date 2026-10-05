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

## Keyboard shortcuts / Raccourcis clavier

Give the Fallout 3 window focus for game shortcuts. Press a combination once to toggle it, then release. VR and tracked weapon control start automatically with **THEwill_Fallout3_VR.exe**.

| Shortcut | Action / Fonction |
| --- | --- |
| **Ctrl+U** | Show/hide gameplay HUD — afficher/masquer les compteurs, boussole et informations du HUD |
| Ctrl+T | Switch smooth / snap turning — rotation fluide / par paliers |
| F10 | Recenter — recentrer (also hold both controller grips for one second) |
| F6 | Toggle VR tracking — activer/désactiver le suivi VR |
| Ctrl+J | Toggle tracked weapon control — suivi de l’arme par la manette |
| Ctrl+H | Toggle independent left-hand preview — suivi indépendant de la main gauche |
| Ctrl+L | Toggle controller locomotion and stick turning — déplacement et rotation aux joysticks |
| Ctrl+B | Enable/disable two-hand grip for the recognized weapon mesh; saved per mesh — autoriser la prise à deux mains pour cette arme |
| Ctrl+Alt+H | Two-step left-hand calibration — tenir la manette dans la pose neutre souhaitée et appuyer, puis tourner jusqu’à ce que la main virtuelle soit correcte et appuyer à nouveau |
| Ctrl+Alt+Shift+H | Reset left-hand calibration — réinitialiser la calibration gauche |
| Ctrl+End | Close the VR scene — fermer la scène VR (quit Fallout normally to finish launcher restoration) |

## Development and comparison shortcuts

These are diagnostic controls, not required for ordinary play. Changing them can deliberately restore rendering defects. Menu/Pip-Boy panels are normally automatic.

| Shortcut | Diagnostic action |
| --- | --- |
| Ctrl+M | Toggle manual floating-panel request |
| Ctrl+W | Compare VR water depth correction with native projection |
| Ctrl+Alt+W | Compare stable water material reflection with native planar reflection |
| Ctrl+Shift+R | Toggle rotational reprojection, enabled by default for SteamVR |
| Ctrl+K | Toggle experimental native hand aim bridge for comparison |
| F8 | Record local render diagnostics; may affect performance |
| Hold F4 | Legacy head-aim test |
| Hold F7 | Legacy shifted-view test |
| Hold F11 | Legacy visibility/culling test; may have no visible effect with automatic corrections active |

Do not publish raw F8 captures: they can contain game meshes and shaders. Share only reviewed screenshots or short log excerpts without personal paths.

New-user calibration and free-hand mesh pose may differ from development videos; no extracted pose data is shipped.
