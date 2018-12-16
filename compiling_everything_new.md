# Compiling Teeworlds 0.7.x

**IMPORTANT NOTE:** SDL and Freetype libs are not shipped with Teeworlds 0.7.x. You must download them separately and place them in the other/ folder.

**Q: What is BAM?**

Bam is the [build system made by matricks](http://matricks.github.io/bam/) used in Teeworlds.

### Setup (Using Microsoft Tools)

1. Download and install [Visual Studio 2017 Community](https://visualstudio.microsoft.com/de/downloads/).


# Compiling Bam

1. Launch `make_win32_msvc.bat` script to compile bam.


# Windows x64 Setup

1. Download and unzip bam to \teeworldsSource\bam
2. Download and install [Python 3.x](https://www.python.org/download/)
3. Download and unzip [Teeworlds](https://github.com/teeworlds/teeworlds/releases) or [Teeworlds-latest-source](https://github.com/teeworlds/teeworlds)
4. Download and unzip [SDL 2.0.8]()
    - Copy "include" and "lib" to \teeworldsSource\other\sdl
    - Copy "SDL2.lib" and "SDL2.main.lib" from \teeworldsSource\other\sdl\win64 in the root directory(\teeworldsSource)
5. Download and unzip [Freetype](https://codeload.github.com/ubawurinna/freetype-windows-binaries/zip/master)
    - Copy "include", "win64" and "win32" to \teeworldsSource\other\freetype
    - Copy "freetype.lib" from \teeworldsSource\other\freetype\win64 in the root directory(\teeworldsSource)


#### Compiling Teeworlds x64

1. Run the `x64 Native Tools Command Prompt` (64Bit) from the start menu.
2. cd "\teeworldsSource" 
    - Changes to the teeworlds source directory
3. .\bam\bam config
    - Runs bam configuration
4. .\bam\bam conf=release -f
    - Compiles teeworlds (Client and Server)
    - Flag -f will force a recompile
    - Available targets:
        - release (for all in release mode)
        - debug (for all in debug mode)
        - server_release
        - server_debug
        - client_release
        - client_debug
    - To build the tools and master server in release mode use the following arguments:
        - conf=release tools masterserver
5. The compiled game is located at \teeworldsSource\build\unknown\...


# Windows x86 Setup

1. Download and unzip bam to \teeworldsSource\bam
2. Download and install [Python 3.x](https://www.python.org/download/)
3. Download and unzip [Teeworlds](https://github.com/teeworlds/teeworlds/releases) or [Teeworlds-latest-source](https://github.com/teeworlds/teeworlds)
4. Download and unzip [SDL 2.0.8]()
    - Copy "include" and "lib" to \teeworldsSource\other\sdl
    - Copy "SDL2.lib" and "SDL2.main.lib" from \teeworldsSource\other\sdl\win32 in the root directory(\teeworldsSource)
5. Download and unzip [Freetype](https://codeload.github.com/ubawurinna/freetype-windows-binaries/zip/master)
    - Copy "include", "win64" and "win32" to \teeworldsSource\other\freetype
    - Copy "freetype.lib" from \teeworldsSource\other\freetype\win32 in the root directory(\teeworldsSource)


#### Compiling Teeworlds x86

1. Run the `x86 Native Tools Command Prompt` (32Bit) from the start menu.
2. cd "\teeworldsSource" 
    - Changes to the teeworlds source directory
3. .\bam\bam config
    - Runs bam configuration
4. .\bam\bam conf=release -f
    - Compiles teeworlds (Client and Server)
    - Flag -f will force a recompile
    - Available targets:
        - release (for all in release mode)
        - debug (for all in debug mode)
        - server_release
        - server_debug
        - client_release
        - client_debug
    - To build the tools and master server in release mode use the following arguments:
        - conf=release tools masterserver
5. The compiled game is located at \teeworldsSource\build\unknown\...

    
