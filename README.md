# Cheatbox

The **Cheatbox** is a collection of cheats and keybinds for Spore that predominantly focus on expanding the functionality of the Editors. 

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

* `Alt+S`. Toggles animations from playing, including the breathing animation of Creatures, and certain motion effects of Building and Vehicle parts.
  * Behaves oddly when switching between Build Mode and Paint Mode for Creatures: the Creature will continue its animation cycle, stopping abruptly after a few seconds. During this time, attempting to add or manipulate parts will be possible, but the parts will either be invisible or changes made will not show up until the Creature stops animating by itself or the action interrupts it as normal. Also does not affect Test Drive Mode.
  * Can be detrimental when dealing with complex Creatures, as animations stopping are an effective way of determining whether or not it has reached the Safe Limit of around 256 parts / rigblocks.
  * Does help when using the Camera Panning bind (`Ctrl+Alt+C`, see below), as it prevents the camera from being recentered whenever a Creature switches animation states.
    
* `Ctrl+Alt+S`. Toggles validation checks, allowing the creation to be saved or loaded where that would normally be possible.
  * Essentially renders Force Save mods obsolete, though itself becomes effectively useless with those mods installed as they hard overwrite the validation checks.
  * Disabling validation checks may have unexpected consequences, namely allowing creations to be saved without a name. Such creations will automatically disappear from the Sporepedia, and will require manual recovery. Use this bind or cheat *only* when you are certain you are ready to save.
  * Overrules the implementation of the `prop` command to toggle validation.
 
* `Ctrl+Shift+S`. Toggles shadows in all modes of the Editor.
  * Does *not* include "painted-on" ambient occlusion shadows cast by parts in Paint Mode.

* `Ctrl+Alt+C`. Toggles camera panning, allowing the camera to be dragged horizontally and vertically while holding `Shift` or `Ctrl` key.
  * `Shift` or `Ctrl` are mutually exclusive, using both will have them cancel each other out.
  * If a Creature switches animation states, the camera will be reset to its original position. Use the Animation Toggle keybind (`Alt+S`) outlined above to work around this.

* `S`. Toggles displaying the Creature's spine. Useful to quickly access it while it's obstructed by parts.

### Misc. Keybinds
Binds that don't belong in the above categories:

* `T`. Switches certain properties of a given part that affects their behaviour when placing them.
  * In Vehicles, this allows Chassis and Cockpits to be placed like Normal Parts and vice-versa.
  * In Creatures, this allows Hands and Feet to be placed like Normal Parts, with some limitations depending on whether or not one has the Spore Stacker mod installed.
  * These property changes *are not retained* when the **Undo** or **Redo** actions are used, nor after reloading a creation, i.e. a Chassis will go back to behaving as it normally does.
  * Creations made using this technique *are* shareable.
    
### Adeventure Editor
Binds specifically for the Adventure Editor:

* `Ctrl+Shift+H`. Toggles displaying *Ghosted* assets, those that are hidden during an act (tinted dark blue), from view in Edit Mode. Useful for previewing without needing to enter Play Mode.
* `Ctrl+Shift+I`. Toggles displaying icons for certain times of assets, namely Audio and Effect assets, at a certain distance.
