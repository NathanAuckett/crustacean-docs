# Level Layout
This page contains information on common conceptsw when layout out levels.

## Character Controller
`obj_characterController`

The character controller is the object representing the player.
This is the object that moves around and interacts with the game world.

## Ground
`obj_ground`

The ground object is an object we can use to easily lay out the ground path for the character controller to follow.
It is invisible when the game runs and acts simply as a pathway.

Its path follows its top edge, stretching to match this object's width and rotating to match its orientation.

A character controller can then walk along the resulting path using horizontal inputs. Left/Right

## Ladder
`obj_ladder`

The ladder is almost identical to the ground.
It acts as a method to easily create vertical paths throughout the game world.

Its path follows its center vertically, stretching to match this object's height and rotating to match its orientation.

A character controller can then walk along the resulting path using vertical inputs. Up/Down

## Path Switcher
`obj_pathSwitcher`

The path switcher does as its name implies and provides a means to set up transitions from one path to another.

This is so that the characterController can move from a horizontal path like ground, to a vertical path like a ladder and vice versa.

The path Switcher contains a number of variables allowing us to control its behaviour:
- pathHorizontal
    - If set, the character controller will move to this path when their feet are touching this collider and a horizontal input is detected.
    - Overrides pathLeft & pathRight
- pathVertical
    - If set, the character controller will move to this path when their feet are touching this collider and a vertical input is detected.
    - Overrides pathUp & pathDown
- pathLeft
- pathRight
- pathUp
- pathDown

For all of the above variables, you may use the following functions as their value:
- `pathInputCollidingGround(optional_ID_String)`
    - Checks for any **ground objects** colliding with the path switcher and if found, will set the path switcher variable to the ground’s path automatically.
    - Can **optionally** specify an Identifier string for the ground if multiple ground objects might be found.<br>This string should be the same as the IDString set on the ground object itself. The string must be encapsulated with quotes: “identification string”
- `pathInputCollidingLadder(optional_ID_String)`
    - Checks for any **ladder objects** colliding with the path switcher and if found, will set the path switcher variable to the ladder’s path automatically.
    - Can **optionally** specify an Identifier string for the ground if multiple ground objects might be found.<br>This string should be the same as the IDString set on the ground object itself. The string must be encapsulated with quotes: “identification string”
