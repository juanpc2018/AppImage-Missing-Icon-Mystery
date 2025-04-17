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
NVIDIA propietary driver seems to piggyback Video Decoding & 3D Acceleration Load using CPU MMX, SSE instructions, </br>
but Nouveau driver does Not, when GPU acceleration works. </br>

20.04 also has i386 installed, have to test again without i386 </br>
but seems 32-Bit AppImages only run in 32-Bit OS, </br>
requires [additional steps](https://github.com/RazZziel/PortableLinuxGames/wiki/Setup-a-64bit-system-to-run-32bit-appimages) to open on 64-Bit OS. </br>

### Untested: </br>
[AMDgpu](https://en.wikipedia.org/wiki/AMDgpu_(Linux_kernel_module)) </br>

## AppImage Icons tested: </br>
#### FAIL 20.04.4 LTS + NV126: </br>
[audacity-linux-3.0.4 to 3.7.0](https://github.com/audacity/audacity/releases/) </br>
[mpv-v0.40.0-42-g36ea2354b-anylinux-x86_64](https://github.com/pkgforge-dev/mpv-AppImage/releases) </br>
[mpv-v0.40.0-42-g36ea2354b-anylinux-x86_64.dwfs.AppBundle](https://github.com/pkgforge-dev/mpv-AppImage/releases) </br>
[OpenSCAD-2021.01-x86_64](https://github.com/openscad/openscad) </br>
unetbootin-linux64-702.bin </br>
unetbootin-linux-702.bin </br>
[qbittorrent-4.6.7 to 5.0.4](https://github.com/qbittorrent/qBittorrent) </br>
[rpcs3-v0.0.36-17785-e80809f6_linux64](https://github.com/RPCS3/rpcs3-binaries-linux/releases?q=build-e80809f62993da0a09cb391576baf3da66e53f66&expanded=true) </br>
[rpcs3-v0.0.36-17784-5ac4db75_linux64](https://rpcs3.net/compatibility?b) </br>
rpcs3-v0.0.36-17783-746b4385_linux64 </br>
rpcs3-v0.0.36-17782-0964c035_linux64 </br>
rpcs3-v0.0.36-17781-7500d165_linux64 </br>
rpcs3-v0.0.36-17779-fcb6bc70_linux64 </br>
rpcs3-v0.0.36-17778-9c5b3a23_linux64 </br>
rpcs3-v0.0.36-17777-2d7ffaf0_linux64 </br>
rpcs3-v0.0.36-17776-9b7d5cd1_linux64 </br>
rpcs3-v0.0.36-17775-bcb5041d_linux64 </br>
[rpcs3-v0.0.36-17774-23570727_linux64](https://github.com/RPCS3/rpcs3-binaries-linux/releases?q=build-235707278fb0126b32cb8892c98a9534c4e6dd1b&expanded=true) </br>

[qjackctl-1.0.4-5.1.x86_64](https://www.appimagehub.com/p/1126620) </br>
 displayed an icon, because it was stored in cache from previous test using NV137 driver, </br>
 icon does Not load anymore on NV126, after copy other .appimage to folder. </br>

[qtractor-1.5.3-10.1.x86_64](https://www.appimagehub.com/p/1126633) </br>
 displayed an icon, because it was stored in cache from previous test using NV137 driver, </br>
 icon does Not load anymore on NV126, after copy other .appimage to folder. </br>

[GIMP 3.0.2](https://edgeuno-bog2.mm.fcix.net/gimp/gimp/v3.0/linux/GIMP-3.0.2-x86_64.AppImage.torrent)

-----------

#### PASS 20.04.4 LTS + NV126: </br>
[audacity-linux-3.7.1-x64-22.04 to 3.7.3](https://github.com/audacity/audacity/releases/) </br> 
3.7.1-20.04 icon FAIL, app works. </br>
3.7.1-22.04 icon Works, app fail. </br>
3.7.2 & 3.7.3 -20.04 & -22.04 Work ok. </br>

[qbittorrent-5.0.3-lt20-x86-64](https://www.appimagehub.com/p/2259406) unofficial appimage icon works, but App does Not, only 4.6.7 work in 20.04 LTS </br>

[rpcs3-v0.0.36-17765-ddf684c4_linux64](https://github.com/RPCS3/rpcs3/releases) </br>
[rpcs3-v0.0.36-17766-58714d8c_linux64](https://rpcs3.net/compatibility?b) </br>
rpcs3-v0.0.36-17767-16036e04_linux64 </br>
rpcs3-v0.0.36-17768-e4d84e2c_linux64 </br>
rpcs3-v0.0.36-17769-87d8bebd_linux64 </br>
rpcs3-v0.0.36-17771-d0861088_linux64 </br>
rpcs3-v0.0.36-17772-15758171_linux64 </br>
[rpcs3-v0.0.36-17773-db855951_linux64](https://github.com/RPCS3/rpcs3-binaries-linux/releases?q=build-db85595124d486792b6efaef1f0ef46384514a99&expanded=true) </br>

[scribus-1.6.3-linux-x86_64](https://sourceforge.net/projects/scribus/files/scribus/1.6.3/) </br>
[scribus-1.7.0-linux-x86_64](https://sourceforge.net/projects/scribus/files/scribus-devel/1.7.0/) </br>
[mpv-x86-64.AppImage](https://www.appimagehub.com/p/2271789) </br>

[balenaEtcher-1.18.12-x64](https://github.com/balena-io/etcher/issues/4265) .13 does Not work in 20.04.4 LTS </br>
but all balenaEtcher have icons up to v2.1.0 </br>

[Inkscape-e7c3feb-x86_64_0QCD8vJ](https://media.inkscape.org/dl/resources/file/Inkscape-e7c3feb-x86_64_0QCD8vJ.AppImage) </br>
kmidimon-1.4.1-x86_64 </br>
[qtractor-1.5.4-11.1.x86_64](https://sourceforge.net/projects/qtractor/files/qtractor/1.5.4/)

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
![image](https://github.com/user-attachments/assets/903d4f4e-7666-483f-8d7c-0287cae1677b) </br>
![image](https://github.com/user-attachments/assets/9c57454e-73cf-4f97-8ac1-abe172220de7) </br>


----------------------------------

# The Conflict

turned-off my 20.04.4 LTS, went to sleep, woke-up, turned-on 20.04.4 LTS </br>
Now.... </br>
Magically.... </br>
Nothing works. LOL  </br>

with 2x exeptions: </br>
OpenSCAD Now works </br>
and InkScape, MidiMon always works. </br>
all other AppImage stop showing icons. </br>

OpenSCAD is the suspect creating the conflict. </br>
have to reboot again, do more tests to confirm. </br>
but its very strange yesterday OpenSCAD icon was Missing, Now is working, but Nothing else works. </br>
maybe is something else, i have to do more tests, but i dont remember installing Nothing. </br>

My guess: seems OS / Nautilus search / index .appimages on the folder everytime there is a change </br>
the 1st appimage it detects, scans for version1 or version2 of AppImageKit,  </br>
loads / scan the icons, </br>
IF following AppImages have a different AppImageKit version, </br>
does Not load / scan / Nor detects icons. </br>
does Not dinamically / individually scan each AppImage version, only the 1st AppImage it detects. </br>

![Screenshot_20250416_171216](https://github.com/user-attachments/assets/845561b3-5389-4c1b-9a2d-c06238d6bda8) </br>
![Screenshot_20250416_171238](https://github.com/user-attachments/assets/d8ce33b0-e887-49b5-83ef-ae58cb395257) </br>
![Screenshot_20250416_171250](https://github.com/user-attachments/assets/6f83d39d-c052-4d88-8778-53e291714ff2) </br>
![Screenshot_20250416_171300](https://github.com/user-attachments/assets/50392df9-b5ec-4ce1-a4c3-38620e6ada20) </br>
![Screenshot_20250416_171312](https://github.com/user-attachments/assets/5974ca7c-13e5-492f-96bc-18be824196b7) </br>
![Screenshot_20250416_171326](https://github.com/user-attachments/assets/ce314271-f246-47bb-9c71-9e6df8d50402) </br>
![Screenshot_20250416_171343](https://github.com/user-attachments/assets/3ad05be6-9e66-4904-a0b7-98f570e5f6ca) </br>


Moved /AppImage Folder to other SSD, and Now 0% icons work.  </br>
it could be a Files/Nautilus 3.36.3-stable problem also.  </br>

have installed latest [Files / Nautilus devel Nightly](https://welcome.gnome.org/app/Nautilus/) </br>
because Normal Files / Nautilus was [deleted](https://flathub.org/apps/search?q=gnome+Nautilus) from Flathub </br>
but No... same result. </br>

moved only /Audacity folder back to /Downloads </br>
and some icons work again... </br>
there is 1 icon different, previously Not visible. </br>

![image](https://github.com/user-attachments/assets/fe954a3c-0d83-4da8-be62-cbd259bb402b) </br>

There is a severe incompatibility between all different versions of AppImageKit  </br>
system does Not know how to handle different versions of AppImageKit </br>
would have to investigate how all versions of AppImageKit work in more depth. </br>
also cache does Not seem to do a good -Recursive search. </br>

latest Files 49.alpha-e739dc7f9 </br>
does Not detect any AppImage icon. </br>

```
$ flatpak install org.gnome.NautilusDevel.flatpakref
The remote 'gnome-nightly', referred to by 'org.gnome.NautilusDevel' at location https://nightly.gnome.org/repo/ contains additional applications.
Should the remote be kept for future installations? [Y/n]: 
Required runtime for org.gnome.NautilusDevel/x86_64/master (runtime/org.gnome.Platform/x86_64/master) found in remote gnome-nightly
Do you want to install it? [Y/n]: 

org.gnome.NautilusDevel permissions:
    ipc     wayland     x11     dri     file access [1]     dbus access [2]     tags [3]

    [1] /tmp, host, xdg-run/dconf, xdg-run/gvfsd, ~/.config/dconf:ro
    [2] ca.desrt.dconf, org.gnome.Console, org.gnome.DiskUtility, org.gnome.Mutter.ServiceChannel, org.gnome.NautilusPreviewer, org.gnome.NautilusPreviewerDevel,
        org.gnome.OnlineAccounts, org.gnome.Settings, org.gtk.MountOperationHandler, org.gtk.vfs.*
    [3] devel, development, nightly


        ID                                              Branch                 Op             Remote                   Download
 1. [✗] org.freedesktop.Platform.GL.default             24.08                  u              flathub                  < 155,7 MB
 2. [✗] org.freedesktop.Platform.GL.default             24.08extra             u              flathub                  < 155,7 MB
 3. [✓] org.freedesktop.Platform.openh264               2.5.1beta              i              gnome-nightly              910,1 kB / 971,2 kB
 4. [✓] org.gnome.NautilusDevel.Locale                  master                 i              gnome-nightly               58,3 kB / 4,7 MB
 5. [✓] org.gnome.Platform.Locale                       master                 i              gnome-nightly              144,7 kB / 387,2 MB
 6. [✓] org.gnome.Platform                              master                 i              gnome-nightly              258,8 MB / 398,0 MB
 7. [✓] org.gnome.NautilusDevel                         master                 i              gnome-nightly                8,0 MB / 11,3 MB

Warning: Server returned status 404: Not Found
Warning: Server returned status 404: Not Found
Changes complete.
```

```
$ flatpak list
Name                                           Application ID                                Version      Branch        Origin                      Installation
default                                        org.freedesktop.Platform.GL.Debug.default                  24.08         flathub                     system
default                                        org.freedesktop.Platform.GL.Debug.default                  24.08extra    flathub                     system
Freedesktop SDK                                org.freedesktop.Platform.GL.default           24.3.4       24.08         flathub                     system
Freedesktop SDK                                org.freedesktop.Platform.GL.default           24.3.4       24.08extra    flathub                     system
openh264                                       org.freedesktop.Platform.openh264             2.4.1        2.4.1         flathub                     system
Cisco Systems, Inc.                            org.freedesktop.Platform.openh264             2.5.1        2.5.1beta     gnome-nightly               system
Files                                          org.gnome.NautilusDevel                       49~alpha     master        gnome-nightly               system
GNOME Application Platform version 47          org.gnome.Platform                                         47            flathub                     system
GNOME Application Platform version Nightly     org.gnome.Platform                                         master        gnome-nightly               system
alsa-scarlett-gui                              vu.b4.alsa-scarlett-gui                                    master        alsa-scarlett-gui-origin    system
```

```
~/Downloads$ flatpak run org.gnome.NautilusDevel

(org.gnome.NautilusDevel:2): GVFS-WARNING **: 18:39:17.917: The peer-to-peer connection failed: Error when getting information for file “/run/user/1000/gvfsd”: No such file or directory. Falling back to the session bus. Your application is probably missing --filesystem=xdg-run/gvfsd privileges.

(org.gnome.NautilusDevel:2): GVFS-WARNING **: 18:39:17.918: The peer-to-peer connection failed: Error when getting information for file “/run/user/1000/gvfsd”: No such file or directory. Falling back to the session bus. Your application is probably missing --filesystem=xdg-run/gvfsd privileges.
** Message: 18:39:17.996: Connecting to org.freedesktop.Tracker3.Miner.Files

(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.320: Theme directory 16x16/panel of theme pearOS-dark has no size field
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.326: Theme directory 16x16@2x/places of theme pearOS-dark has no size field
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.328: Theme directory 24x24/apps of theme pearOS-dark has no size field
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.331: Theme directory 24x24@2x/panel of theme pearOS-dark has no size field
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.332: Theme directory 24x24@2x/panel of theme pearOS-dark has no size field
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.682: Theme directory 16x16/panel of theme pearOS-dark has no size field
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.686: Theme directory 16x16@2x/places of theme pearOS-dark has no size field
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.688: Theme directory 24x24/apps of theme pearOS-dark has no size field
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.691: Theme directory 24x24@2x/panel of theme pearOS-dark has no size field
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:18.691: Theme directory 24x24@2x/panel of theme pearOS-dark has no size field
** (org.gnome.NautilusDevel:2): WARNING **: 18:39:18.827: Unable to get contents of the bookmarks file: Error opening file /home/jpc/.var/app/org.gnome.NautilusDevel/config/gtk-3.0/bookmarks: No such file or directory
** (org.gnome.NautilusDevel:2): WARNING **: 18:39:18.850: Unable to create connection for session-wide Tracker indexer: GDBus.Error:org.freedesktop.DBus.Error.ServiceUnknown: The name org.freedesktop.portal.Tracker was not provided by any .service files
** Message: 18:39:18.850: Starting org.gnome.NautilusDevel.Tracker3.Miner.Files
(org.gnome.NautilusDevel:2): GVFS-WARNING **: 18:39:19.914: The peer-to-peer connection failed: Error when getting information for file “/run/user/1000/gvfsd”: No such file or directory. Falling back to the session bus. Your application is probably missing --filesystem=xdg-run/gvfsd privileges.
** (org.gnome.NautilusDevel:2): CRITICAL **: 18:39:19.914: Could not start local Tracker indexer at org.gnome.NautilusDevel.Tracker3.Miner.Files: GDBus.Error:org.freedesktop.DBus.Error.ServiceUnknown: The name org.freedesktop.portal.Tracker was not provided by any .service files
(org.gnome.NautilusDevel:2): GVFS-WARNING **: 18:39:19.966: The peer-to-peer connection failed: Error when getting information for file “/run/user/1000/gvfsd”: No such file or directory. Falling back to the session bus. Your application is probably missing --filesystem=xdg-run/gvfsd privileges.
(org.gnome.NautilusDevel:2): GVFS-WARNING **: 18:39:19.999: The peer-to-peer connection failed: Error when getting information for file “/run/user/1000/gvfsd”: No such file or directory. Falling back to the session bus. Your application is probably missing --filesystem=xdg-run/gvfsd privileges.
(org.gnome.NautilusDevel:2): GVFS-WARNING **: 18:39:20.000: The peer-to-peer connection failed: Error when getting information for file “/run/user/1000/gvfsd”: No such file or directory. Falling back to the session bus. Your application is probably missing --filesystem=xdg-run/gvfsd privileges.
(org.gnome.NautilusDevel:2): GVFS-WARNING **: 18:39:20.284: The peer-to-peer connection failed: Error when getting information for file “/run/user/1000/gvfsd”: No such file or directory. Falling back to the session bus. Your application is probably missing --filesystem=xdg-run/gvfsd privileges.
(org.gnome.NautilusDevel:2): GVFS-WARNING **: 18:39:20.322: The peer-to-peer connection failed: Error when getting information for file “/run/user/1000/gvfsd”: No such file or directory. Falling back to the session bus. Your application is probably missing --filesystem=xdg-run/gvfsd privileges.
(org.gnome.NautilusDevel:2): GVFS-WARNING **: 18:39:20.324: The peer-to-peer connection failed: Error when getting information for file “/run/user/1000/gvfsd”: No such file or directory. Falling back to the session bus. Your application is probably missing --filesystem=xdg-run/gvfsd privileges.
(org.gnome.NautilusDevel:2): Gtk-WARNING **: 18:39:23.383: Failed to load icon /run/host/share/icons/breeze/mimetypes/64/application-pgp-encrypted.svg: Error opening file /run/host/share/icons/breeze/mimetypes/64/application-pgp-encrypted.svg: Too many levels of symbolic links
```
![image](https://github.com/user-attachments/assets/32bcd5e4-9838-485b-8369-211e96cf4deb) </br>

----------------

# Conclusion

their plan seem to be converting everything to Go generic language easy for A.i.  </br>
and want A.i. to magically solve all problems.  </br>
LOL </br>

