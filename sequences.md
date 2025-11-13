# Sequences

Sequences in game maker are animations created through key frames and tweening(generating in-between frames).<br>
They allow for sprites, objects and more to be animated with fine control through different tracks, a bit like a movie editor.<br>
Sounds can also be triggered via sequences by placing them at specific times on the timeline.

These sequences can be used for a number of things such as, but not limited to, cutscene creation.

Sequences play out their timeline at a set speed by default.<br>
You can set their length and the sequence will play from start to finish unless interrupted via external means(*code*).<br>
Sequences can be made to loop and play back and forth too.

## Controlling sequences
In most cases a sequence will only need to play forward in time and stop at the end.

For things like waiting for input, I've set up some extra controls to start with, but more can be added as requirements are identified.

### Controls <!-- {docsify-ignore} -->
- Pause sequence until an input is pressed.
    - Useful for if the player needs to acknowledge something before proceeding.
- Jump to a specific time/frame in the sequence, skipping forward or back.
    - Useful for skipping cutscenes, or situations where part of a sequence should only play when a condition is met.


## Sequence Moments
A sequence moment is a key frame on the timeline that executes some code.

The code can be anything and its useful for things such as:
- Telling the camera to follow the sequence camera target(`obj_sequeneMarker_cameraTarget`), or resetting the camera to follow the player again at the end of a sequence.
- Triggering camera shake.
- Triggering sequence control objects like pausing or jumping to a point.
- Triggering conditional things like different sounds or particle effects.


## Sequence Objects
A number of objects have been created as placeholders specifically for use within sequences.

obj_sequenceMarker_player1
To be used as a placeholder for player 1’s character controller. Can be overridden/replaced when the sequence plays in game.
obj_sequenceMarker_player2
To be used as a placeholder for player 2’s character controller. Can be overridden/replaced when the sequence plays in game.
obj_sequeneMarker_cameraTarget
An object to act as the target position for the game’s camera, allowing the camera to be moved within the sequence, pointing towards this object's position as the sequence plays.
