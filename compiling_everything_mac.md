# Compiling Teeworlds on Mac

**IMPORTANT NOTE:** SDL and Freetype libs are not shipped with Teeworlds 0.7.x. You must download them separately.

**Q: What is BAM?**

Bam is the [build system made by matricks](http://matricks.github.io/bam/) used in Teeworlds.

#### Setup
1. Install Xcode from the Appstore or install Xcode Command Line Tools `xcode-select --install`. 
3. Install libsdl using [brew](https://brew.sh/) `brew install sdl2`
4. Install Freetype using [brew](https://brew.sh/) `brew install freetype`
5. Download and unzip [Teeworlds-source](https://github.com/teeworlds/teeworlds/releases) or [Teeworlds-latest-source](https://github.com/teeworlds/teeworlds)
6. Download and unzip [bam](https://github.com/matricks/bam/archive/v0.5.1.zip) to `\teeworldsSource\bam`
7. Compiling bam  
    - `$ cd bam`
    - `$ ./make_unix.sh`
    - `$ cd ..`

#### Compiling
2. `cd /teeworldsSource`
    - Changes to the teeworlds source directory
3. `./bam/bam config`
    - Runs bam configuration
4. `./bam/bam conf=release -f`
    - Compiles teeworlds (Client and Server)
    - Flag `-f` will force a recompile
    - Available targets:
        - `release` (for all in release mode)
        - `debug` (for all in debug mode)
        - `server_release`
        - `server_debug`
        - `client_release`
        - `client_debug`
    - To build the tools and master server in release mode use the following arguments:
        - `conf=release tools masterserver`
        
5. The compiled game is located at `/teeworldsSource/build/..`



# For Teeworlds v0.6.x and earlier

Available targets are:

+ release (for all in release mode)
+ debug (for all in debug mode)
+ server_release
+ server_debug
+ client_release
+ client_debug

E.g. to build server debug use the following arguments:

`../bam/bam server_debug`

**Also:** Teeworlds 0.5.2 and earlier requires python 2.x to compile. Python 3.x will not work. Python 3.x support is introduced with Teeworlds 0.6.0.

**Also:** If you are using bam 0.2.0 (needed for Teeworlds 0.5.2 and earlier) the bam binary will not be in the bam directory, but in bam/src. You will need to change the paths accordingly to that or copy/move the bam executable to the bam directory.

