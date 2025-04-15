# AppImage Missing Icon Mystery

have Noticed something strange... </br>
downloading many [AppImages](https://www.appimagehub.com/browse) </br>

0% AppImages have Icon on 20.04.6 LTS "File Manager Large Icon View Nautilus" </br>
50% AppImages show icon on 22.04 LTS, 50% don't.</br>
100% has icons on 24.04 LTS </br>

using different Nvidia Propietary drivers 470 510 525 535 </br>
older drivers are "incomplete". </br>
BUT...</br>
Nouveau NV137 driver: all AppImage icons show on 20.04.4 LTS </br>
Nouveau NV126 driver: 25% AppImage icons Do Not show on 20.04.4 LTS </br>

the only way fixing this problem: </br>
"becoming an AppImage that has icon on 22.04 using Nvidia driver"</br>
or </br>
"becoming an AppImage that has icon on 20.04 using Nouveau NV126 driver"</br>
is using an older AppImageKit version </br>
a different package method like [Sharun](https://github.com/VHSgunzo/sharun) may Not work on NV126 </br>

reading [wikipedia](https://en.wikipedia.org/wiki/AppImage) </br>
in 2004 AppImage started as Klik </br>
in 2011 was renamed as PortableLinuxImage, created a web with [537 games](https://portablelinuxgames.org/) </br>
in 2013 was renamed as AppImage </br>
in 2016 version 2 renamed as AppImageKit </br>
in 2025 renamed as [AppImageTool](https://github.com/AppImage/appimagetool/releases/tag/continuous) </br>

version 1 was ISO 9660 CD-Rom image, </br>
version 2 has [SquashFS](https://en.wikipedia.org/wiki/SquashFS) type FileSystem "Read Only FileType" </br>
similar to snap, but portable. </br>

Official links: </br>
https://appimage.org/ </br>
https://github.com/AppImage/AppImageKit </br>
https://github.com/AppImage/AppImageKit/blob/master/README.md </br>

The oldest AppImageKit Prerelease-1 has a [.pdf](https://github.com/AppImage/AppImageKit/releases/download/1/AppImage.Mythbusting.2020.pdf)
PreRelease-5 also has a [PDF](https://github.com/AppImage/AppImageKit/releases/download/5/AppImage.pdf)


### NV137 gpus tested:  </br>
GTX 1050 Ti </br>
Quadro P400 </br>

### NV126 gpus tested: </br>
Quadro M2000 </br>
all have icons in 20.04.4 LTS </br>

### FAIL: </br>
Quadro 6000 (2010) Nouveau driver has "Pink Screen of Death" in 20.04.4 LTS </br>

P400 requires a fast board & CPU, Nouveau driver NV137 lacks optimization, has poor video playback on YouTube, skips frames, etc... </br>
latest Windows8.1x64 driver works better, but... sometimes crash & reboots the system. </br>

20.04 also has i386 installed, have to test again without i386 </br>
but seems 32-Bit AppImages only run in 32-Bit OS, </br>
requires [additional steps](https://github.com/RazZziel/PortableLinuxGames/wiki/Setup-a-64bit-system-to-run-32bit-appimages) to open on 64-Bit OS. </br>

### Untested: </br>
AMD gpu </br>
