# Wineskin
Wineskin is a user-friendly tool used to make ports of Microsoft Windows software to macOS.\
Unlike the original [Wineskin Project](http://wineskin.urgesoftware.com) by doh123 that worked on *OS X 10.6* to *macOS 10.12* (without tweaks), this project supports *MacOSX10.13* to *macOS11*

<br>

## How to install
### [homebrew](https://brew.sh/)
```
brew install --no-quarantine gcenx/wine/unofficial-wineskin
```

### Manual installation - (_not recommneded!_)  
[Download Wineskin Winery v1.8.4.2](https://github.com/Gcenx/WineskinServer/releases/download/V1.8.4.2/Wineskin.Winery.txz)\
*_After downloading remove the flag quarantine before extraction, don't extract using __Keka___
```
xattr -drs com.apple.quarantine Wineskin.Winery.txz
```

<br>

## DirectX support
WineD3D by default converts D3D to OpenGL, OpenGL on macOS hasn't been updated in years, at present only __DirectX9__ and earlier function.\
__DXVK__ Requirements are not entirely known at this time, however as CodeWeavers locks support to macOS High Sierra this would be a good start.\
Open the winetricks menu and select one of the provided DXVK macOS verbs.\
For older wrappers ensue you've updated winetricks to get my forked version.

This will install DXVK for __DirectX 10__ and __DirectX 11__ support for 64Bit games.\
__32Bit DirectX10 and later is not supported on macOS__\
__VKD3D is no supported!__

<br>

## Apple Silicon support (Rosetta2)
The only Engine(s) that fully function to on these devices is WineCX20.0.4 or greater.\
This will require macOS Big Sur 11.1 or greater and Rosetta2 needs to be installed.

<br>

## macOS Catalina support
__WS11WineCX19.0.4__ & __WS11WineCX64Bit19.0.4__ include `wine32on64` meaning they function on macOS Catalina. 10.15.4 or greater.\
All future __WS11__ Engines automatically mean Catalina is supported.

<br>

### macOS Catalina (10.15.3 and below)
SIP needs to be disabled to make changes to `i386_set_ldt` for `wine32on64` to function.\
__This configuration is not supported, upgrade to macOS Catalina 10.15.4 or greater.__

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
This started once wine moved to using *Mingw-gcc* to compile PE binaries.

__See the following examples__
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
