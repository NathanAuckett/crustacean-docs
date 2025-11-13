# Audio

Audio is played via audio emitters and the game has one audio listener.

The audio listener follows the center point of the camera at all times.

## Global Audio Emitters
Global audio emitters follow the center point of the camera at all times ensuring **they are full volume and not impacted by position within the world**.<br>
Global audio emitters are specifically designed to be used for when audio should be full volume no matter its source.

There is a global audio emitter for each audio type:
- Sounds
- Voice
- Music

There are helper functions for playing sounds from the pre-made global emitters:
```gml
audio_play_sound_on_soundGlobal(_sound, _loop = false, _priority = 0, _gain = 1, _pitch = 1)
audio_play_sound_on_voiceGlobal(_sound, _loop = false, _priority = 0, _gain = 1, _pitch = 1)
audio_play_sound_on_musicGlobal(_sound, _loop = false, _priority = 0, _gain = 1, _pitch = 1)
```

## Standard Audio Emitters
Standard, non-global audio emitters can be created on any instance within the game and they will be impacted by their position/distance to the audio listener.
- Sounds further away are quieter.
- Sounds to the right come from the right speaker/headphone, and vice versa.