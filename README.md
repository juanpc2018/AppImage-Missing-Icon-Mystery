# AppImage Missing Icon Mystery

have Noticed something strange... </br>
downloading many [AppImages](https://www.appimagehub.com/browse) </br>

0% AppImage has Icon on Dolphin / Nautilus  20.04.6 LTS </br>
50% AppImages show icon in 22.04 LTS, 50% don't.</br>
100% show icons in 24.04 LTS </br>
...</br>
using different Nvidia Propietary drivers 470 510 525 535 </br>
drivers are "incomplete",</br>

Nouveau NV137 driver NV137: all AppImage icons show in 20.04.4 LTS</br>
BUT...</br>
Not all AppImage icons show using Nouveau driver NV126</br>


the only way fixing the problem "becoming the 50% AppImage that shows icon on 22.04"</br>
is using a different / older AppImageKit version</br>
a different package method like [Sharun](https://github.com/VHSgunzo/sharun) may Not work on NV126 </br>

reading [wikipedia](https://en.wikipedia.org/wiki/AppImage) </br>
AppImage started as Klik in 2004, </br>
was renamed as PortableLinuxImage in 2011, created a web with [537 games](https://portablelinuxgames.org/) </br>
in 2013 was renamed as AppImage </br>
in 2016 version 2 renamed as AppImageKit </br>
2025 latest version renamed as [AppImageTool](https://github.com/AppImage/appimagetool/releases/tag/continuous) </br>
*i don't like rolling releases. </br>

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
Quadro 6000 (2010) Nouveau driver has Pink Screen of Death in 20.04.4 LTS </br>


20.04 also has i386 installed, have to test again without i386 </br>
but seems 32-Bit AppImages only run in 32-Bit OS, </br>
requires [additional steps](https://github.com/RazZziel/PortableLinuxGames/wiki/Setup-a-64bit-system-to-run-32bit-appimages) to open on 64-Bit OS. </br>
