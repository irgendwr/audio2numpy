# audio2numpy
[![Build Status](https://travis-ci.com/irgendwr/audio2numpy.svg?branch=master)](https://travis-ci.com/irgendwr/audio2numpy)

## Description

audio2numpy load an audio file and directly ouputs the audio data as a numpy array and its sampling rate. Supports `.wav`, `.aiff` via python's standard library, and other formats via [ffmpeg](https://ffmpeg.org/).

## Installation

Using pip:

`pip install git+https://github.com/irgendwr/audio2numpy`

## FFmpeg for decoding mp3

audio2numpy requires ffmpeg to decode mp3 files. You would need to install ffmpeg in order to have mp3 support. 

### macOS

`homebrew install ffmpeg`

### Linux

  - Debian/Ubuntu: `sudo apt-get install ffmpeg`
  - Arch: `sudo pacman -S ffmpeg`

[Check here](https://www.ostechnix.com/install-ffmpeg-linux/) for other installation methods for different Linux distributions. 

### Windows

  1. [Download ffmpeg](https://ffmpeg.org/download.html)
  2. Extract it into a folder, for example `C:\FFmpeg`
  3. Add the ffmpeg bin folder to your PATH Environment Variable.

[Here](https://www.thewindowsclub.com/how-to-install-ffmpeg-on-windows-10) is a guide that explains the process in detail.

### Colab

`!apt install ffmpeg`

## Usage

```python
from audio2numpy import open_audio
path = "./examples/word.mp3"
signal, sampling_rate = open_audio(path)
```

## Version History

**0.1.4 (09.09.2021)**
  - Remove format limitation: [wiccy46/audio2numpy#2](https://github.com/wiccy46/audio2numpy/pull/2)

**0.1.3 (17.10.2019)**
  - Add Colab ffmpeg installation guide. 
  - Remove ffmpeg from requirements.txt. Users should install it separately

**0.1.2 (20.08.2019)**

Add instructions to install ffmpeg if load mp3 failed with ffmpeg backend not available.

**0.1.1 (14.08.2019)**

Initial release.
