# Add Camera Shake to a Clip

* Setup your sequencer, add a camera (drag it from Outliner), and set up a camera pan/animation
* Add a CameraShakeBase Blueprint class
* William's suggestion is to open the blueprint, close it, and open it again so it just shows the data part of the blueprint.
* Set **Camera Shake Pattern** to Perlin Noise Camera Shake Pattern
* Set Timing > Duration to 0, so it wil shake the entire length of your video (infinitely). Otherwise the setting is in seconds.
* Try: Compile and apply the camera shake so far to your camera.
* Select the **CameraComponent** in the the Sequencer.
* Add a CameraShake track, and you should be able to choose the blueprint you just created.
  * Check that the shake track stretches all the way to the end of the timeline.
* In the blueprint, set Rotation > Rotation Amplitude Multiplier to 1. You can set it to 10 as an experiment ;).
  * Amplitude sets how big the shake is, Frequency sets how often the shake occurs.
  * Starting point: Amplitude = 0.2, Frequency = 2.0

## Rotation Settings

Pitch: Controls the camera shake up and down.
Yaw: Controls the camera shake left and right.

* A pro tip is to have 2 camera shake actors stacked in the timeline.
* Use the first one for a baseline, gentle shake, and the second for more smaller "micro" shakes.

