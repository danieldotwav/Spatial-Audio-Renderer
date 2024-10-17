# Real-Time Spatial Audio Renderer

## Overview

This project is a real-time spatial audio renderer built using C++ and OpenAL. It simulates 3D sound environments for gaming applications, utilizing advanced audio techniques such as beamforming and reverberation to create an immersive experience. Additionally, it aims to integrate support for Dolby Atmos, providing a rich multi-channel audio experience.

## Features

- **3D Sound Rendering**: Play audio in a 3D space, simulating realistic positions and movements.
- **Beamforming Simulation**: Use beamforming to control audio directionality and enhance spatial audio accuracy.
- **Reverberation Effects**: Apply environmental reverberation to enhance audio realism.
- **OpenAL Integration**: Built using OpenAL, a cross-platform 3D audio API for efficient audio rendering.

## Project Structure

The project consists of several key components:

1. **Initialization**: The `InitOpenAL` function initializes OpenAL, creating a device and context for audio processing.
2. **Listener Configuration**: The `ConfigureListener` function sets up the listener's position, velocity, and orientation in the 3D space.
3. **Audio Loading and Playback**: The `LoadSoundBuffer` function loads audio data, and the `Create3DSource` function sets up and plays the audio in 3D space.
4. **Effects and Beamforming**:
   - **Reverb**: The `ApplyReverb` function uses OpenAL's Effects Extension (EFX) to apply reverberation effects to audio sources.
   - **Beamforming**: The `BeamformAudio` function controls the directionality of audio playback, simulating beamforming to enhance spatial audio perception.

## Getting Started

### Prerequisites

- **C++ Compiler**: Ensure you have a C++ compiler like GCC or MSVC.
- **OpenAL**: Install OpenAL (https://openal.org/downloads/).
- **OpenAL EFX**: The OpenAL Effects Extension is required for reverberation.

### Running the Project

1. Ensure OpenAL is correctly installed and available on your system.
2. Compile the C++ source files:
   ```sh
   g++ -o spatial_audio_renderer main.cpp -lopenal
   ```
3. Run the executable:
   ```sh
   ./spatial_audio_renderer
   ```

### Audio Files

The `LoadSoundBuffer` function expects audio files in `.wav` format. Place your audio files in the project directory and modify the `LoadSoundBuffer` function to load the desired file.

## Usage

- **3D Listener Setup**: The listener is positioned at the origin, facing along the negative Z-axis.
- **Reverb and Beamforming**: Reverberation and beamforming can be adjusted for different effects. Modify parameters in `ApplyReverb` and `BeamformAudio` for custom configurations.

## Future Enhancements

- **Dolby Atmos Integration**: Add support for Dolby Atmos for a multi-channel 3D audio experience.
- **HRTF (Head-Related Transfer Function)**: Implement HRTF to further enhance the spatial audio experience.
- **Real-Time Audio Processing**: Expand the real-time loop for dynamic audio adjustments based on game events.

## Dependencies

- **OpenAL**: Cross-platform 3D audio API.
- **libsndfile (Optional)**: To handle loading of different audio file formats.

## Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue for any improvements or bug fixes.

