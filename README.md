## Wineskin Unofficial Update
A working version of Wineskin using the development code from [Wineskin](https://github.com/vitor251093/wineskin) with some tweaks, the [Original Wineskin Code](https://sourceforge.net/p/wineskin/code) was updated by [VitorMM](https://github.com/vitor251093) and some additional features and fixes by myself [Unoffical_Wineskin](https://github.com/vitor251093/wineskin/tree/Unoffical_Wineskin).  
Unlike the [Official Wineskin Project](http://wineskin.urgesoftware.com) by doh123 that worked on *OSX 10.6* to *macOS 10.12* (without tweaks), this project supports *MacOSX10.9* to *macOS10.14*

## Contained here;
1) Wine versions packaged as *Engines* to be used with `Wineskin Winery`
2) WineskinWinery.app - *The current version will be downloaded updating the local version*
3) Wineskin Unofficial Updates - *Master Wrapper*

## Currently available compiled Wine Versions (Engines)
- WS11WineCX64Bit19.0.1 *(10.8 > 10.15)*
- WS11WineCX19.0.1      *(10.8 > 10.15)*
- WS10WineCX64Bit18.5.0 *(10.8 > 10.14)*
- WS10WineCX18.5.0      *(10.8 > 10.14)*

*All other Wine versions are repacked from [Winehq](https://dl.winehq.org/wine-builds/macosx/pool/) portable releases into Wineskin Engines*  
This occurred in your system.

### OS X Mountain Lion (10.8) support;
Due to changes with secure connections on GitHub `Wineskin Winery` will no longer function, the master wrapper would need to be downloaded manually and `EngineList.txt` placed next to `Wineskin Winery` in order for it to function. WineCX engines will also need to be downloaded manually.  
Winehq repacking *should* still function until that also migrates to requiring a higher SSL/TLS version for secure connections.

## macOS Catalina support;
__WS11WineCX19.0.1__ & __WS11WineCX64Bit19.0.1__ include `wine32on64` meaning they function on macOS Catalina but as they have not been code-signed & notarized additional steps are required.  
All future __WS11__ Engines automatically mean Catalina is supported.

### macOS Catalina (10.15.4);
Setting `no32exec=0` boot argument allows changes to `i386_set_ldt` meaning `wine32on64` will function.

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
- [val1984](https://github.com/val1984) for noticing the change in `no32exec=0` behavior allowing changes to `i386_set_ldt` with SIP enabled in macOS Catalin 10.15.4

Want to help support this project?  
[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/gcenx?locale.x=en_US)
