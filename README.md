# Cheatbox

The **Cheatbox** is a collection of cheats and keybinds for Spore that predominantly focus on expanding the functionality of the Editors.

**Note**: this mod *must* be installed with either the [Spore ModAPI Launcher Kit](https://davoonline.com/sporemodder/rob55rod/ModAPI/Public/), or [Spore Mod Loader](https://github.com/Rosalie241/SporeModLoader), and can only be used when running the game with the respective programs. Running the game normally will not cause issues, but will *not* allow the cheats and keybinds to be used.

**WARNING: This mod does not work for the October 2024 updated version of Spore on Steam distributions due to the incompatibility of that version with the ModAPI Launcher Kit and Mod Loader.**

# Features

## Keybinds
The mod includes a number of keybinds, sequences of keys that when pressed perform a certain function. Each keybind also has an attached cheat that does the same as the bind in the event that the keybind is unavailable for some reason, such as being tied to something else outside of Spore, also including in some circumstances sound cues and/or on-screen hints for feedback. 

**Note:** all of these keys are *single-fire*, meaning they don't need to be held.

Among the binds and their respective cheats, there are:

### Hide Parts ("Masking")
Using a series of keybinds revolving around the `L` button, users can now selectively hide parts *in Build Mode* for a variety of purposes, namely reaching parts made inaccessible by other parts, quickly accessing the skin, etc.:
  
* The keybinds are activated only when interacting with a selected part, or when the cursor is hovering over a part (indicated by a subtle blue tint on the hovered part). *A selected part takes priority over a hovered part for hiding*:
  * The `L` key, when pressed, will hide the selected/hovered part from view while the creation is stationary in Build Mode. If the creation is an animating Creature, once the Creature starts animating, the part will be rendered visible again until the animation is interrupted and it returns to its "edit pose".
    * Pressing `Alt+L` will hide the part symmetrically.
  * Pressing `Ctrl+L` will reveal *all* hidden parts.
  * Pressing `Shift+L` will hide the given part, and all parts attached to it sequentially. 
    * Pressing `Shift+Alt+L` will do the above symmetrically.
  * Pressing `Ctrl+Shift+L` will hide all regular placeable parts, except the limbs and the vertebra pieces of a Creature.

* Can also be used on Building and Vehicle parts, even in the Paintbrush mode of Paint Mode.
  
* Part hiding *does not* persist in Paint Mode, Test Drive Mode, or outside of the Editor.

### Editor Properties
A set of keybinds that change the functioning of the Editor itself:

* ~~`Alt+S`. Toggles animations from playing, including the breathing animation of Creatures, and certain motion effects of Building and Vehicle parts.~~
  * ~~Behaves oddly when switching between Build Mode and Paint Mode for Creatures: the Creature will continue its animation cycle, stopping abruptly after a few seconds. During this time, attempting to add or manipulate parts will be possible, but the parts will either be invisible or changes made will not show up until the Creature stops animating by itself or the action interrupts it as normal. Also does not affect Test Drive Mode.~~
  * ~~Can be detrimental when dealing with complex Creatures, as animations stopping are an effective way of determining whether or not it has reached the Safe Limit of around 256 parts / rigblocks.~~
  * ~~Does help when using the Camera Panning bind (`Ctrl+Alt+C`, see below), as it prevents the camera from being recentered whenever a Creature switches animation states.~~
  * Temporarily Disabled due to unexplained crashes. See **Config Tweaks** below for an alternative.*
    
* `Ctrl+Alt+S`. Toggles validation checks, allowing the creation to be saved or loaded where that would normally be impossible.
  * Essentially renders Force Save mods obsolete, though itself becomes effectively useless with those mods installed as they hard overwrite the validation checks.
  * Disabling validation checks may have unexpected consequences, namely allowing creations to be saved without a name. Such creations will automatically disappear from the Sporepedia, and will require manual recovery. Use this bind or cheat *only* when you are certain you are ready to save.
  * Overrules the implementation of the `prop` command to toggle validation if using that particular tweak.
 
* `Ctrl+Shift+S`. Toggles shadows in all modes of the Editor.
  * Does *not* include "painted-on" ambient occlusion shadows cast by parts in Paint Mode.

* `Ctrl+Alt+C`. Toggles camera panning, allowing the camera to be dragged horizontally and vertically while holding `Shift` or `Ctrl` key.
  * `Shift` or `Ctrl` are mutually exclusive, using both will have them cancel each other out.
  * ~~If a Creature switches animation states, the camera will be reset to its original position.~~
  * If using Dark Injections's Flexible Camera component, the vertical panning is broken.

* `S`. Toggles displaying the Creature's spine. Useful to quickly access it while it's obstructed by parts.

* `Ctrl + G`. Toggle a highly-customiseable placement grid in the Editor. Use the `editorGrid` cheat to customise it, enter `help editorGrid` for detailed instructions.

* `Ctrl + B`. Executes the `toggleeditorbackground` cheat to do exactly as the cheat's name implies.

* `Ctrl + NUMPAD`. Snap to a preset view in the Editor.
  * WARNING: This cheat and associated keybinds have been known to cause unexpected, non-replicable crashes in certain contexts, use with caution.
  * The "reset" bind may behave oddly when using the Panning bind/cheat mentioned above.

  * `Ctrl + NUMPAD_8`. Top-down view.
  * `Ctrl + NUMPAD_2`. Bottom-up view.
  * `Ctrl + NUMPAD_4`. Right-side profile view.
  * `Ctrl + NUMPAD_6`. Left-side profile view.
  * `Ctrl + NUMPAD_5`. Front-side view.
  * `Ctrl + NUMPAD_0`. Back-side view.
  * `Ctrl + NUMPAD_*`. Manually center the camera so the creation is in the middle of the screen.
  * `Ctrl + NUMPAD_.`. Reset the camera view to its default offset and rotation.
    * Note: can cause odd behaviour when switching modes.

### Misc. Keybinds
Binds that don't belong in the above categories:

* `T`. Switches certain properties of a given part that affects their behaviour when placing them.
  * In Vehicles, this allows Chassis and Cockpits to be placed like Normal Parts and vice-versa.
  * In Creatures, this allows Hands and Feet to be placed like Normal Parts, with some limitations depending on whether or not one has the Spore Stacker mod installed.
  * **Note**: These property changes *are not retained* when the **Undo** or **Redo** actions are used, nor after reloading a creation, i.e. a Chassis will go back to behaving as it normally does.
  * Creations made using this technique *are* shareable within certain limitations.

* `Ctrl + M`. Toggles music and ambience globally, including Dark Injection ambience in the Hero Editor if that particular mod component happens to be installed.

### Adventure Editor
Binds specifically for the Adventure Editor:

* `Ctrl+Shift+H`. Toggles displaying *Ghosted* assets, those that are hidden during an act (tinted dark blue), from view in Edit Mode. Useful for previewing without needing to enter Play Mode.
* `Ctrl+Shift+I`. Toggles displaying Icons for certain times of assets, namely Audio and Effect assets, at a certain distance.

## Cheats
True to the name of the mod, it contains over two dozen-or-so cheats. This list can be viewed in-game by entering `help_cheatbox` into the console. Use `help <cheatname>` for more specific information about each cheat, this list also contains the keybind (in brackets) associated with the same function where applicable.

**Note**: the droplist is huge and won't render properly if the console window is too thin, expand it horizontally if needed.

### Hide Part Cheats:
* `hideSelectedPart` (`L`). Hides the *selected* part. Use with option `-sym` for symmetrical hiding.
* `hideSelectedPartChain` (`Shift+L`). Hides the *selected* part and all parts attached to it. Use with option `-sym` for symmetrical hiding.
* `hideHoveredPart` (`L`). Hides the *hovered* part. Use with option `-sym` for symmetrical hiding.
* `hideHoveredPartChain` (`Shift+L`). Hides the *hovered* part and all parts attached to it. Use with option `-sym` for symmetrical hiding.
* `hideAllParts` (`Ctrl + Shift+L`). Hides all parts except for certain types of Limbs and Creature vertebrae.
* `unhideParts` (`Ctrl+L`). Unhides all hidden parts.

### Editor Cheats:
* ~~`toggleEditorAnimations` (`Alt+S`). Toggles animations in Build Mode.~~
* `toggleForceSave` (`Ctrl+Alt+S`). Toggles validation checks when saving or loading creations.
* `toggleSpine` (`S`). Toggles displaying the spine of a Creature.
* `toggleEditorShadows` (`Ctrl+Shift+S`). Toggles in-editor shadows.
* `toggleEditorCamPanning` (`Ctrl+Alt +C`). Toggles camera drag-panning with Shift or Ctrl.
* `togglePartOTS` (`T`). Changes the behaviour of the selected or hovered part when placing it.
* `playModeLighting`. Lists or sets the lighting environment of the Play Mode environment. (experimental; background lighting currently not affected)
* `setPartBools`. Lists or sets some properties of a part. (experimental)
* `editorManipulators`. Lists, sets, adds or removes certain Editor functions, such as limb manipulation. (experimental)
* `editorView` (`Ctrl + NUMPAD`). System of preset views and options to alter the camera's position and behaviour. Requires *NumLock* to be active. (experimental)"
* `editorGrid` (`Ctrl + G`). Enables a highly-customiseable grid effect for precision placement. Available in all Editors but most useful for buildings. (Requires Dependencies Package included with v1.2.2r)
* `editorSkybox -colour`. Sets the colour of the void behind the background, useful when used with the bind below. (Requires Dependencies Package included with v1.2.2r)

### Adventure Cheats:
* `captainPos`. Sets the position, rotation and scale of the captain in all Adventure modes.
  * `-set`
    * `-position`. Sets the (absolute) position of the avatar (not adjusted for planetary coordinates) in all modes (Vector3).
    * `-rotation`. Sets the (absolute) rotation of the avatar in all modes (Vector3).
    * `-size`. Sets the (relative) size of the avatar in all modes (float).
  * `-get`
    * `-position`. Gets the position of the avatar.
    * `-rotation`. Gets the rotation of the avatar.
    * `-size`. Gets the rotation of the avatar.
* `getAdventureData`. Displays some basic debug information about the adventure.
* `setAdventureCam`. Sets the position, rotation and distance of the Edit Mode camera when used in Play Mode. (experimental)
* `resetAdventureCam`. Resets the adventure camera to a safe position when run from Play Mode in the event of bugs.
* `toggleGhostedObjects` (`Ctrl+Shift+H`). Toggles displaying act-hidden (blue tinted) objects in Edit and Terraform mode.
* `toggleHiddenAEIcons` (`Ctrl+Shift+I`). Toggles displaying icons for certain assets at a distance.

### Other Cheats:
* `getCamData`. Displays some basic debug information about the camera, including adventure-specific info when in that Editor.
* `toggleMusic` (`Ctrl + M`). Globally mutes music or returns it to the value specified in Settings. Also mutes Dark Injection Hero Editor ambience, if present.
* `help_cheatbox`. Displays this list.

## Config Tweaks
As of version 1.2.2r, the Cheatbox now includes a system to read configurations from Spore's Config folder. These allow users to set specific options relating to cheats added by the mod.

If you have used the HD Texture Fix, you should know how this works, but to briefly explain: Add these to the respective files in `[Galactic Adventures]/DataEP1/Config`, *or* create a new `.txt` for each (i.e. `Custom_props.txt` and `Custom_config.txt`) in the same `Config` folder and use `sinclude` in the respective original files to add them. (i.e. at the bottom of Properties.txt, add: `sinclude "Custom_props.txt"` and then do the same for the Configs).

In `Properties.txt`:

```
### Editor Grid
property editorGridOpacity (hash(gridOpacity)) float 0.55 # set the default opacity the grid should start with when entering the editor
property editorGridShape (hash(gridShape)) key 0x215A5A88.rw4 # the grid's default shape / texture when entering the editor

### Editor Limits
# the following are applied regardless of editor, 
property editorDefaultPartLimit (hash(editorDefaultPartLimit)) int 250 # how many parts are allowed to be placed in the editor;  beware shennanigans with splitting parts, they can go over the limit somehow
property editorDefaultComplexity (hash(editorDefaultComplexity)) int 280 # default complexity to budget to set when entering any editor
property editorDefaultBudget (hash(editorDefaultBudget)) int 99999 # default amount of DNA / currency to set when entering any editor

# force the game to load this specific limit when entering the editor (every time)
# overwrites the specific default limit configs above, except budget
property forceEditorLimit (hash(forceEditorLimit)) int 0  # 0 - none, 1 - vanilla, 2 - vanilla + freedom, 3 - safe, 4 - unlimited
```

In `ConfigManager.txt`:

```
### Editor Grid
floatProp editorGridOpacity 0.55 # 55% Opacity, *not* 55% Transparency (Opaque = 100% visible, Transparent = 0% visible)
keyProp editorGridShape editorgrid_circle.rw4 # 0x0!0x16D0DAED.0x2F4E681B

### Editor Limits
intProp editorDefaultPartLimit 255 # max parts *before* animations stop
intProp editorDefaultComplexity 2147483646 # basically infinite
intProp editorDefaultBudget 99999 

intProp forceEditorLimit 0
```

## Known Issues
These issues are known (most of them noted above) and being worked on when time permits. Do not create Issue threads about them.

* ~~Camera Panning resets to center when Creature starts animating. (appears to be related to more complicated functions, may not be fixable)~~
  * v1.2.2r addresses this issue in a roundabout manner, but may be subject to change depending on how stable this workaround proves to be.
* `Alt+S` keybind and cheat crashes to desktop when used. (this is well known and cannot be properly replicated. Therefor both the bind and the cheat have been disabled until a solution is found)
  * In the meantime, one can do further config tweaking to enable the use of this function via the `prop` cheat:
    * In `[Galactic Adventures]\DataEP1\Config\Properties.txt`, add the line: `property EditorAnimateWhileEditing 55 bool true` at the bottom of the file.
    * In `[Galactic Adventures]\DataEP1\Config\ConfigManager.txt`, add the line: `boolProp EditorAnimateWhileEditing true` at the bottom of the file. Set to `false` to disable animations on startup.
    * In the console, enter `prop EditorAnimateWhileEditing` to toggle the animations. Animations already playing will continue to play until an editting action is performed, and similarly will not start again when re-enabled until an action is performed.
* Part OTS setting does not persist after Undo and/or Redo are used. (this is true for most properties covered under `setPartBools`)
* `playModeLighting` does not affect backgrounds. (this seems to be a problem with the model used by the background not having the right shader properties to be tinted)

**Note**: Open-source project files pending. Finalising comments.

## Special Thanks
* [emd4600](https://github.com/emd4600). Creator of the Spore ModAPI SDK.
* [Liskomato](https://github.com/Liskomato). Bug and feature testing; advice and code snippets.
* [ThePlantGuy](https://www.spore.com/view/myspore/adam215jj). Bug and feature testing.
