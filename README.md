## Wineskin Unofficial Update
A working version of Wineskin using the development code from [Wineskin](https://github.com/vitor251093/wineskin) with some tweaks, the [Original Wineskin Code](https://sourceforge.net/p/wineskin/code) was updated by [VitorMM](https://github.com/vitor251093) and some additional features and fixes by myself [Unoffical_Wineskin](https://github.com/vitor251093/wineskin/tree/Unoffical_Wineskin).  
Unlike the [Official Wineskin Project](http://wineskin.urgesoftware.com) by doh123 that worked on *OS X 10.6* to *macOS 10.12* (without tweaks), this project supports *MacOSX10.9* to *macOS11*

![Downloads count](https://img.shields.io/github/downloads/gcenx/wineskinserver/total.svg)

## Contained here;
1) Wine versions packaged as *Engines* to be used with `Wineskin Winery`
2) WineskinWinery.app - *The current version will be downloaded updating the local version*
3) Wineskin Unofficial Updates - *Master Wrapper*

## Currently available compiled Wine Versions (Engines)
- WS11WineCX64Bit19.0.1-1 *(10.9 > 10.15)*
- WS11WineCX19.0.1-1      *(10.9 > 10.15)*
- WS10WineCX64Bit18.5.0   *(10.9 > 10.14)*
- WS10WineCX18.5.0        *(10.9 > 10.14)*

*All other Wine versions are repacked from [Winehq](https://dl.winehq.org/wine-builds/macosx/pool/) portable releases into Wineskin Engines*  
This repacking is done on your system.

## DirectX support and wine
Wine converts D3D to OpenGL and the version on macOS hasn't been updated in years, at present only __DirectX9__ and earlier functions.\
__DirectX10 and later are not supported on macOS__\
__DXVK & VKD3D are also no supported!__

## Apple Silicon support (Rosetta2);
This will require access to one of these devices.\
The only Engine(s) that will fully function to on these devices will be WineCX20.0.1 or greater.\
This will require macOS Big Sur 11.1 or greater and Rosetta2 needs to be installed.\
However ddraw and direct3d won't function currently so things like cnc-ddraw and DxWnd need to be used\
to play older titles, but newer titles like Fallout New Vegas will function.

## macOS Catalina support;
__WS11WineCX19.0.1-1__ & __WS11WineCX64Bit19.0.1-1__ include `wine32on64` meaning they function on macOS Catalina but as they have not been code-signed & notarized additional steps are required.  
All future __WS11__ Engines automatically mean Catalina is supported.

### macOS Catalina (10.15.4 and later);
Setting `no32exec=0` boot argument avoids Gatekeeper warning when running 32Bit executables.\
It's still recommended currently to disable SIP, due to the additional restrictions on user directories an example being `~/Downloads`\
Currently looking into some different options to correctly handle obtaining permission to these locations even if a user didn't allow it initially.

### macOS Catalina (10.15.3 and below);
SIP needs to be disabled to make changes to `i386_set_ldt` for `wine32on64` to function.

## Hackintosh Support?
__AMD__ based systems are not supported due to being unable to run 32Bit code on macOS.  
__Intel__ based systems should work without issue.

## License
Keeping the same as the original material, LGPL 2.1 is the license of that project. You can find more details about that in the LICENSE file.

## Credits
- [VitorMM](https://github.com/vitor251093) for modernizing the [Wineskin Codebase](https://github.com/vitor251093/wineskin) & [ObjectiveC_Extension](https://github.com/vitor251093/ObjectiveC_Extension)
- [PaulTheTall](https://www.paulthetall.com/) for constant test data and finding bugs
- doh123 for creating [Wineskin](http://wineskin.urgesoftware.com).
