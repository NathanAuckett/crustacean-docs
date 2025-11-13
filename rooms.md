# Rooms

Rooms, in Game Maker, are where all game elements come together to form a level.<br>
Everything in the game occurs within a room, from gameplay to UI elements.

Technically you can only ever be within one room at a time.

## Creating a new room <!-- {docsify-ignore} -->
To create a new room, duplicate the existing “rm_base”.<br>
*We do this to ensure a minimum set of layers exist in every part of the game.*

To duplicate, simply right click rm_base in the resource tree and select “duplicate”.<br>
Give the new room a new name, starting with "rm_", *which denotes this game resource is a room*.<br>
For example: `rm_myCoolLevel`