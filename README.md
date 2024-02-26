# Nova
PaxOS 8 is the latest version of PaxOS, a lightweight operating system for PaxoPhones.

Build Instructions
Linux
Windows
MacOS
License
Contact
See more
Contributors
Build Instructions
The paxos offers a multi-platform emulator so that you can run it directly on your computer. In this section you will find instructions on how to build it for your operating system.

Linux
Before you start, make sure that git, cmake and make are correctly installed on your computer. If not, install them using the command sudo apt install build-essential (if you use apt as your package manager).

You can then start the build instructions :

Clone the directory using git clone https://github.com/paxo-phone/paxos_8.git
Move to the newly created folder using cd paxos_8/
Load the sub-modules using git submodule init && git submodule update
Compile the project using cmake . && make
Run the executable using ./PaxOS
The emulator should then open in a window.

Windows
Before getting started, you need an IDE and know how to setup a CMake project with custom toolchain.

Install CMake and MinGW
Setup your favorite IDE 'CLion' with MinGW (recommended) 'Visual Studio Code' with MinGW (https://code.visualstudio.com/docs/cpp/config-mingw)
Setup CMake using Ninja (recommended)
You shouldn't have to install any library (everything is included)
MacOS
The instructions for building under macos are fairly similar to those under Linux.

Before you start, make sure that git, cmake and make are correctly installed on your computer. If not, you can use the brew package manager to install them using the following command brew install cmake make git.

You can then start the build instructions :

Clone the directory using git clone https://github.com/paxo-phone/paxos_8.git
Move to the newly created folder using cd paxos_8/
Load the sub-modules using git submodule init && git submodule update
Compile the project using cmake . && make
Run the executable using ./PaxOS
The emulator should then open in a window. Press the 'Escape' key to emulate the 'Home' button.

Troubleshooting :

If you get the message ld: warning: ignoring file /opt/homebrew/Cellar/sdl2/2.28.2/lib/libSDL2-2.0.0.dylib': found architecture 'arm64', required architecture 'x86_64' followed by an error you can do:
cp src/lib/SDL2-2.28.2/libSDL2-2.0.0-2.dylib /opt/homebrew/Cellar/sdl2/2.28.2/lib/libSDL2-2.0.0.dylib
Disable the quarantine for the file: xattr -dr com.apple.quarantine /opt/homebrew/Cellar/sdl2/2.28.2/lib/libSDL2-2.0.0.dylib
If you get the message  Could not find a package configuration file provided by "SDL2" with any of the following names::
Add -DCMAKE_PREFIX_PATH=src/lib/SDL2-2.28.2/ to your cmake command.
