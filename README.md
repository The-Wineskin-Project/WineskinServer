## Wineskin Unofficial Update
A working version of Wineskin using the development code from [Wineskin](https://github.com/vitor251093/wineskin) with some tweaks, the [Original Wineskin Code](https://sourceforge.net/p/wineskin/code) was updated by [VitorMM](https://github.com/vitor251093) and some additional features and fixes added by myself.
Unlike the [Official Wineskin Project](http://wineskin.urgesoftware.com) by doh123 that worked on *MacOSX10.6*, the project here will only function on *MacOSX10.8* and above due to the included dylib versions.

## Contained here;
1) Wine versions packaged as *Engines* to be used with "Wineskin Winery"
2) WineskinWinery.app - Current versions to be downloaded to update the local version
3) Wineskin Unoffical Update's - Master Wrapper

## Currently avaliable compiled Wine Versions (Engines)
- WS10WineCX64Bit18.1.0
- WS10WineCX18.1.0
- WS10WineCX64Bit18.0.0
- WS10WineCX18.0.0
- WS9WineCX64Bit17.5.1
- WS9WineCX17.5.1
- WS9WineCX64Bit17.5.0
- WS9WineCX17.5.0

*Other Wine versions are repacked from [Winehq](https://dl.winehq.org/wine-builds/macosx/pool/) into Engines*

## Issues with custom engines!
All custom engines are compiled on macOS using Apple Clang, however this causes some [issues](https://wiki.winehq.org/Clang) that means some features will not work like official versions from WineHQ.
I'm looking into building wine using real gcc on macOS or just resort to [cross-compiling](https://github.com/wine-compholio/wine-packaging) using docker.

## License
Keeping the same as the original material, LGPL 2.1 is the license of that project. You can find more details about that in the LICENSE file.

## Credits
- [VitorMM](https://github.com/vitor251093) for modernizing the [Wineskin Codebase](https://github.com/vitor251093/wineskin) & [ObjectiveC_Extension](https://github.com/vitor251093/ObjectiveC_Extension)
- Special thanks to doh123, for creating [Wineskin](http://wineskin.urgesoftware.com/tiki-index.php).
