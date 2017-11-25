# Panda3D Third-party

## Build Status

| OS       | Build Status             | Latest Build                                                  |
| :------: | :----------------------: | :-----------------------------------------------------------: |
| Windows  | [![win-badge]][win-link] | vc14 ([MixForDebug][win-mixfordebug], [Release][win-release]) |

[win-badge]: https://ci.appveyor.com/api/projects/status/4bq68rpiw5dr27y4/branch/develop?svg=true "AppVeyor build status"
[win-link]: https://ci.appveyor.com/project/bluekyu/panda3d-thirdparty/branch/develop "AppVeyor build link"
[win-mixfordebug]: https://ci.appveyor.com/api/projects/bluekyu/panda3d-thirdparty/artifacts/panda3d-thirdparty.7z?branch=develop&job=Configuration%3A+MixForDebug "Download latest build (MixForDebug)"
[win-release]: https://ci.appveyor.com/api/projects/bluekyu/panda3d-thirdparty/artifacts/panda3d-thirdparty.7z?branch=develop&job=Configuration%3A+Release "Download latest build (Release)"

##### Note
- These builds are default builds, not everything. So, some files may be omitted.
- Windows MixForDebug is a configuration composed of debug (Assimp, OpenEXR) and release (others) libraries.
  This is used in Panda3D Debug.



## Guide
This repository contains a CMake script to build the thirdparty packages that
are necessary for building Panda3D.

Usage example:

    mkdir build
    cd build
    cmake -DCMAKE_BUILD_TYPE=Release -G"Visual Studio 14 2015 Win64" ..
    cmake --build . --config Release

To build with Visual Studio 2015 for 64-bit Windows XP, change the command to:

    cmake -DCMAKE_BUILD_TYPE=Release -G"Visual Studio 14 2015 Win64" -DCMAKE_SYSTEM_VERSION=5.2 -T v140_xp ..

To build with Visual Studio 2015 for 32-bit Windows XP, change the command to:

    cmake -DCMAKE_BUILD_TYPE=Release -G"Visual Studio 14 2015" -DCMAKE_SYSTEM_VERSION=5.1 -T v140_xp ..

Some packages are still forthcoming.  The included packages are ticked.
- [x] artoolkit
- [x] assimp (except Mac)
- [x] bullet
- [x] eigen
- [x] fcollada
- [x] ffmpeg (except Windows)
- [ ] fmodex
- [x] freetype
- [x] jpeg
- [x] nvidiacg
- [x] ode
- [x] openal
- [x] openexr
- [x] openssl (except Mac)
- [x] png
- [ ] rocket
- [x] squish
- [x] tiff
- [x] vorbis
- [x] vrpn
- [x] zlib
