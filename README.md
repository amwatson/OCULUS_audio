# OCULUS_audio

## Contributors

* Amanda Watson, Oculus, <mailto:amanda.watson@oculus.com>

## Status

Draft (not ratified yet)

## Dependencies

Written against the glTF draft 1.0 spec.

## Overview
This extension adds general support for spatialized audio in glTF scenes.  Audio sources are specified at the node level, and are colocated with the location of their node/joint in worldspace.       

| Property                     | Type         | Description | Default Value |
|:----------------------------:|:------------:|:-----------:|:-------------:|
| `source`                    |  string | The audio source ID | None |
| `volume`                    |  `float` | The factor by which the audio source's volume is scaled for playback. An Audio source with volume 0.0 is considered to be disabled, and may be ignored | 0.0 |
| `reflection`                    |  string | Audio source attenuation mode | false |
| `attenuation`                    |  `boolean` | Denotes whether reflection should be enabled (true) or disabled (false) | 'NONE' |
| `diameter`                    |  `float` | Virtual diameter of the spherical audio source in meters. Larger sizes provide more envelopment for volumetric sounds | 0.0 |
| `maxSpeed`                    |  `float` | Max speed at which the audio source can travel, in meters/second. Unanticipated jumps in motion may produce artifacts during positional interpolation | 0.0 |
| `startOffset`                    |  `float` | The number of seconds between the time at which audio playback is requested, and the start time of the given audio source. If 'loop' is set to true, the audio source will restart playback 'startOffset' seconds after the end time of the previous iteration | 0.0 | 
| `loop`                    |  `boolean` | When true, the audio source is played continuously in a loop, restarting 'startOffset' seconds after the previous iteration has completed | false |

### JSON Schema

* <a href="schema/audio.schema.json">`audio`</a>
* <a href="schema/node.OCULUS_audio.schema.json">`node/audio`</a>
