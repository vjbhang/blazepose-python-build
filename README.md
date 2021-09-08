# README

## Instructions

### Media Pipe Initialization

1. [Bazel and OpenCV configurations for MediaPipe](https://google.github.io/mediapipe/getting_started/install.html)

   1. Install MSYS2 and edit `%PATH%` environment variable
   2. `pacman -S git patch unzip` in MSYS2
   3. Set Python 3.7
   4. Install Visual C++ Build Tools 2019 and WinSDK (Computer Restart)
   5. Install Bazelisk
      - Install Go v1.11 or greater
      - in `cmd`
        - `go install github.com/bazelbuild/bazelisk@latest`
        - `bazelisk`
   6. set Bazel variables
   7. Checkout MediaPipe repository
   8. Install OpenCV 3.4.10 [here](https://opencv.org/releases/)
   9. Run the Hello World! in C++ example.
      - I had to manually find where the Bazel.exe was downloaded from based on Go Bazelisk.
      - Then I set an alias to that .exe location to run from my git bash
        - run command in /mediapipe
        - `bazel build -c opt --define MEDIAPIPE_DISABLE_GPU=1 --action_env PYTHON_BIN_PATH="C://python_36//python.exe" mediapipe/examples/desktop/hello_world`
