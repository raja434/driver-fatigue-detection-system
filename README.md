# driver-fatigue-detection-system
drowsiness detection

# Intallation process

## step 1:
 Install all libraries 
 - scipy  (pip install scipy)
     - We’ll need the SciPy package so we can compute the Euclidean distance between facial landmarks points in the eye aspect ratio calculation (not strictly a requirement, but you should have SciPy installed if you intend on doing any work in the computer vision, image processing, or machine learning space).

- OpenCv
  - openCv for computer vision

- numpy (pip install numpy)
  - numpy for basic processing and calcutions ...

- imutils (pip install imutils)
   - We’ll also need the imutils package, my series of computer vision and image processing functions to make working with OpenCV easier.

-  pyglet (pip install pyglet)
    - we'll also need pyglet  playing sound such as .mp3 , .wav ...  

-  dlib
   - To detect and localize facial landmarks we’ll need the dlib library


# installation of Dlib libary 
These instructions assume you are on macOS, but basically the same on Linux.

Pre-reqs:
- Have Python 3 installed. On macOS, this could be installed from homebrew or even via standard 
  Python 3.6 downloaded installer from https://www.python.org/download. On Linux, just use your
  package manager.
- On macOS:
  - Install XCode from the Mac App Store (or install the XCode command line utils).
  - Have [homebrew](https://brew.sh/) installed
  - Install boost with this command: `brew install boost-python --with-python3 --without-python`
- On Linux:
  - Install boost. On Ubuntu, that's `sudo apt-get install libboost-all-dev`
- This assumes you don't have an nVidia GPU and don't have Cuda and cuDNN installed and don't want
  GPU acceleration (since none of the current Mac models support this).
- On Windows:
  - Please follow this link to install dlib on Windows: https://www.learnopencv.com/install-dlib-on-windows/

Clone the code from github:

```bash
git clone https://github.com/davisking/dlib.git
```

Build the main dlib library:

```bash
cd dlib
mkdir build; cd build; cmake .. -DDLIB_USE_CUDA=0 -DUSE_AVX_INSTRUCTIONS=1; cmake --build .
```

Build and install the Python extensions:

```bash
cd ..
python3 setup.py install --yes USE_AVX_INSTRUCTIONS --no DLIB_USE_CUDA
```

At this point, you should be able to run `python3` and type `import dlib` successfully.

# if you have python 2.7.---
```bash
cd ..
python setup.py install --yes USE_AVX_INSTRUCTIONS --no DLIB_USE_CUDA
```
# step 2
- Download the dlib’s pre-trained facial landmark detector. from hear "http://jmp.sh/4bIYiPU " place it place it same floder where alarm.wav contains 

- Note: without dlib’s pre-trained facial landmark detector file you can't run the code 

# step 3

```bash
python drowsiness detection.py

```
