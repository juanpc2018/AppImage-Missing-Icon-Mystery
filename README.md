# AppImage Missing Icon Mystery

have Noticed something strange... </br>
downloading many [AppImages](https://www.appimagehub.com/browse) </br>

0% AppImages have Icon on 20.04.6 LTS "File Manager Large Icon View Nautilus" </br>
50% AppImages show icon on 22.04 LTS, 50% don't.</br>
100% has icons on 24.04 LTS </br>

using different Nvidia Propietary drivers 470 510 525 535 </br>
older drivers are "incomplete". </br>
BUT...</br>
[Nouveau NV137](https://nouveau.freedesktop.org/CodeNames.html#nv110familymaxwell) driver: all AppImage have icons on [20.04.4 LTS](https://archive.org/details/pearOS_Monterey_64bit-12-beta-2021.07.01) </br>
Nouveau NV126 driver: 25% AppImage icons Do Not show on 20.04.4 LTS </br>

the only way fixing this problem: </br>
"becoming an AppImage that has icon on 22.04 using Nvidia driver"</br>
&/or </br>
"becoming an AppImage that has icon on 20.04 using Nouveau NV126 driver"</br>
is using a Different AppImageKit version, sometimes older, sometimes newer. </br>
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
https://en.wikipedia.org/wiki/Nouveau_(software) </br>
https://nouveau.freedesktop.org/FeatureMatrix.html </br>
https://nouveau.freedesktop.org/VideoAcceleration.html </br>
https://nouveau.freedesktop.org/ </br>

The oldest AppImageKit Prerelease-1 has a [.pdf](https://github.com/AppImage/AppImageKit/releases/download/1/AppImage.Mythbusting.2020.pdf) PreRelease-5 also has a [PDF](https://github.com/AppImage/AppImageKit/releases/download/5/AppImage.pdf)


### NV137 gpus tested:  </br>
[GTX 1050 Ti (2016)](https://www.techpowerup.com/gpu-specs/geforce-gtx-1050-ti.c2885) </br>
[Quadro P400 (2017)](https://www.techpowerup.com/gpu-specs/quadro-p400.c2934) </br>

### NV126 gpus tested: </br>
[Quadro M2000 (2016)](https://www.techpowerup.com/gpu-specs/quadro-m2000.c2837) </br>

### FAIL: </br>
[Quadro 6000 (2010)](https://www.techpowerup.com/gpu-specs/quadro-6000.c896) Nouveau driver [NVC0GL](https://nouveau.freedesktop.org/CodeNames.html#NVC0) has "Pink Screen of Death" on [20.04.4 LTS](https://archive.org/details/pearOS_Monterey_64bit-12-beta-2021.07.01) </br>

P400 requires a fast board & CPU, Nouveau driver NV137 lacks optimization, has poor video playback on YouTube, skips frames, etc... </br>
latest Windows8.1x64 driver works better, but... sometimes crash & reboots the system. </br>
seems [FireFox](https://www.mozilla.org/en-US/firefox/all/desktop-release/) minimum Requirements for YouTube are 8-core CPU + gpu with PCIe v3, maybe 4GB of VRaM also. </br>
NVIDIA propietary driver seems to piggyback video & 3D acceleration load using CPU SSE instructions, </br>
but Nouveau driver does Not, when GPU acceleration works. </br>

20.04 also has i386 installed, have to test again without i386 </br>
but seems 32-Bit AppImages only run in 32-Bit OS, </br>
requires [additional steps](https://github.com/RazZziel/PortableLinuxGames/wiki/Setup-a-64bit-system-to-run-32bit-appimages) to open on 64-Bit OS. </br>

### Untested: </br>
[AMDgpu](https://en.wikipedia.org/wiki/AMDgpu_(Linux_kernel_module)) </br>

### AppImage Icons tested: </br>
#### FAIL 20.04.4 LTS + NV126: </br>
[audacity-linux-3.0.4 to 3.7.0](https://github.com/audacity/audacity/releases/) </br>
[mpv-v0.40.0-42-g36ea2354b-anylinux-x86_64](https://github.com/pkgforge-dev/mpv-AppImage/releases) </br>
[mpv-v0.40.0-42-g36ea2354b-anylinux-x86_64.dwfs.AppBundle](https://github.com/pkgforge-dev/mpv-AppImage/releases) </br>
[OpenSCAD-2021.01-x86_64](https://github.com/openscad/openscad) </br>
unetbootin-linux64-702.bin </br>
unetbootin-linux-702.bin </br>
qbittorrent-4.6.7 to 5.0.4 </br>

[qjackctl-1.0.4-5.1.x86_64](https://www.appimagehub.com/p/1126620) </br>
 displayed an icon, because it was stored in cache from previous test using NV137 driver, </br>
 icon does Not load anymore on NV126, after copy other .appimage to folder. </br>

[qtractor-1.5.3-10.1.x86_64](https://www.appimagehub.com/p/1126633) </br>
 displayed an icon, because it was stored in cache from previous test using NV137 driver, </br>
 icon does Not load anymore on NV126, after copy other .appimage to folder. </br>

#### PASS 20.04.4 LTS + NV126: </br>
[audacity-linux-3.7.1-x64-22.04 to 3.7.3](https://github.com/audacity/audacity/releases/) </br> 
3.7.1-20.04 icon FAIL, app works. </br>
3.7.1-22.04 icon Works, app fail. </br>
3.7.2 & 3.7.3 -20.04 & -22.04 Work ok. </br>

rpcs3-v0.0.36-17765-ddf684c4_linux64 </br>
scribus-1.6.3-linux-x86_64 </br>
scribus-1.7.0-linux-x86_64 </br>
[mpv-x86-64.AppImage](https://www.appimagehub.com/p/2271789) </br>
balenaEtcher-1.18.12-x64  </br>
Inkscape-e7c3feb-x86_64_0QCD8vJ </br>
kmidimon-1.4.1-x86_64 </br>

system icon: </br>
warpinator-android_1.4.6.apk </br>
xyz.pearos.pairdrop.apk </br>
.exe installers like Nvidia or AMD drivers. </br>
.bmp .pdf .jpg .webp </br>

Links: </br>
https://github.com/mpv-player/mpv </br>
TBA... </br>

![image](https://github.com/user-attachments/assets/1a7367db-17ec-4647-9305-446cd0f88d22) </br>
![image](https://github.com/user-attachments/assets/4320c410-5fd9-4fd6-a797-e1ca2b360f04) </br>
