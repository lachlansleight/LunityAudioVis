# Lunity AudioVis

## Installation & Setup

Simply import this entire repository into your Unity project. Drag the SoundCapture prefab into your scene to set up audio capture. Upon entering play mode, you should see the various audio data properties animating in the inspectors of the `SoundCapture` and `AudioAverageSet` components!

This repository is kept minimal, intended to be used in your own scripting projects. The main useful properties for visualization are:

  * `AverageVolume`: The RMS average volume for the most recent frame of audio data. Found on the `SoundCapture` component
  * `PeakVolume`: The peak volume across the `SoundCapture` component's audio bins
  * `BarData`: Individual FFT frequency bins - useful if you are interested in specific frequency ranges
  * The various average values calculated on the `AudioAverageSet` component - you can disable or remove this component if you only care about the per-frame data. These values are smoothed out and can be more useful for some visualization purposes.
  
Note that the values `Flicker`, `Pulse` and `Vibe` on the `AudioAverageSet` component are examples - you can easily create your own composite values to extract certain higher-level visualization 'concepts' out of the raw data!
