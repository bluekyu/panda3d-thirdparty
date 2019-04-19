# Panda3D Third-party

## Build Status

| Build Status                       | About                       |
| :--------------------------------: | :-------------------------: |
| [![azure-badge]][azure-link]       | Visual Studio 2015 and 2017 |
| [![appveyor-badge]][appveyor-link] | Visual Studio 2017 Preview  |

[azure-badge]: https://dev.azure.com/bluekyu/rpcpp-devops/_apis/build/status/panda3d/panda3d-thirdparty?branchName=master
[azure-link]: https://dev.azure.com/bluekyu/rpcpp-devops/_build/latest?definitionId=2&branchName=master
[appveyor-badge]: https://ci.appveyor.com/api/projects/status/4bq68rpiw5dr27y4/branch/master?svg=true "AppVeyor build status"
[appveyor-link]: https://ci.appveyor.com/project/bluekyu/panda3d-thirdparty/branch/master "AppVeyor build link"

You can download built files from each Build Page.



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
- [x] ffmpeg
- [ ] fmodex
- [x] freetype
- [x] harfbuzz
- [x] jpeg
- [x] nvidiacg
- [x] ode
- [x] openal
- [x] openexr
- [x] openssl
- [x] opus
- [x] png
- [ ] rocket
- [x] squish
- [x] tiff
- [x] vorbis
- [x] vrpn
- [x] zlib

A package can be explicitly disabled using the `BUILD_*` options, eg. `-DBUILD_VRPN=OFF` disables building VRPN.  Note that some packages have dependencies on other packages, so not all combinations are valid.

To build nothing but eg. vrpn, specify: `-DDISABLE_ALL=ON -DBUILD_VRPN=ON`.  This only affects the initial configuration.
