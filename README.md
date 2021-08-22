## Wineskin Unofficial Update
A working version of Wineskin using the development code from [Wineskin](https://github.com/vitor251093/wineskin) with some tweaks, the [Original Wineskin Code](https://sourceforge.net/p/wineskin/code) was updated by [VitorMM](https://github.com/vitor251093) and some additional features and fixes by myself [Unoffical_Wineskin](https://github.com/vitor251093/wineskin/tree/Unoffical_Wineskin).  
Unlike the [Official Wineskin Project](http://wineskin.urgesoftware.com) by doh123 that worked on *OS X 10.6* to *macOS 10.12* (without tweaks), this project supports *MacOSX10.13* to *macOS11*

<br>

### Install using [homebrew](https://brew.sh/)
```
brew tap gcenx/wine
brew install --no-quarantine unofficial-wineskin
```
<br>

### Manually installation  
[Download Wineskin Winery v1.8.4.2](https://github.com/Gcenx/WineskinServer/releases/download/V1.8.4.2/Wineskin.Winery.txz)  
![Downloads count](https://img.shields.io/github/downloads/gcenx/wineskinserver/total.svg)

<br>

## Contained here;
1) Wine versions packaged as *Engines* to be used with `Wineskin Winery`
2) WineskinWinery.app - *The current version will be downloaded updating the local version*
3) Wineskin Unofficial Updates - *Master Wrapper*

<br>

## DirectX support and wine
Wine converts D3D to OpenGL and the version on macOS hasn't been updated in years, at present only __DirectX9__ and earlier function.\
__DXVK__ Requirements are not entirely known at this time, however as CodeWeavers locks support to macOS High Sierra this would be a good start.\
To make use of DXVK use a 64Bit WS10 or greater engine, open winetricks and run the following custom command;
```
dxvk_macos.verb
```
This will install DXVK for DirectX10 and DirectX11 support for 64Bit games.\
__32Bit DirectX10 and later is not supported on macOS__\
__VKD3D is no supported!__

<br>

## Apple Silicon support (Rosetta2);
The only Engine(s) that fully function to on these devices is WineCX20.0.4 or greater.\
This will require macOS Big Sur 11.1 or greater and Rosetta2 needs to be installed.\
__However__ older games that use are fullscreen at lower screen resolutions will fail as the\
Apple GPU doesn't seem to support these, using things like `cnc-ddraw` or `DxWnd` to workaround this.

<br>

## macOS Catalina support;
__WS11WineCX19.0.2-2__ & __WS11WineCX64Bit19.0.2-2__ include `wine32on64` meaning they function on macOS Catalina but as they have not been code-signed & notarized additional steps are required.  
All future __WS11__ Engines automatically mean Catalina is supported.

<br>

### macOS Catalina (10.15.3 and below);
SIP needs to be disabled to make changes to `i386_set_ldt` for `wine32on64` to function.\
I don't recommend this configuration so won't provide instructions instead upgrade to macOS Catalina10.15.4 or greater.

<br>

## GateKeeper
Windows applications are not code-signed in a way that GateKeeper understands.\
Either remove the quarantine flag using `xattr -drs com.apple.quarantine {exe here}`\
or disable GateKeeper entirely by running the following
```
sudo spctl --master-disable
```
__*Disabling GateKeeper is not recommended*__

<br>

## Hackintosh Support?
__AMD__ based systems are not supported due to being unable to run 32Bit code on macOS.  
__Intel__ based systems should work without issue.

<br>

# FAQ
### My Antivirus says it's a VIRUS!!!
You need to contact your AntiVirus/AntiMalware vender to connect these false positives.\
This started once wine moved to using *Mingw-gcc* to compile PE binaries.\

__See the following examples;__
- [CrossOver 19 and anti virus programs](https://www.codeweavers.com/support/forums/general/?t=27;msg=222870)
- [Windows Defender detects Occamy.c trojan in steam proton 5.0 folder](https://github.com/ValveSoftware/Proton/issues/3593)

<br>

## License
Keeping the same as the original material, LGPL 2.1 is the license of that project. You can find more details about that in the LICENSE file.

<br>

## Credits
- [VitorMM](https://github.com/vitor251093) for modernizing the [Wineskin Codebase](https://github.com/vitor251093/wineskin) & [ObjectiveC_Extension](https://github.com/vitor251093/ObjectiveC_Extension).
- [PaulTheTall](https://www.paulthetall.com/) for constant test data and finding bugs.
- doh123 for creating [Wineskin](http://wineskin.urgesoftware.com).
- [thmrtz](https://github.com/thmrtnz) for the issue template, documention and the wiki.
