---
title: "Run PSX in Retroach"
layout: post
---

You do to have is download an appimage or install the package .dpkg from [https://buildbot.libretro.com/nightly/linux/x86_64/RetroArch.7z](https://buildbot.libretro.com/nightly/linux/x86_64/RetroArch.7z).

You do have to set appimage properties > execute only the propietary.

Into the retroarch system you have to download a PSX core called:
-  Desktop x86 or x64 is: **Beetle PSX HW**
-  For Android or ARM based: **PCSX ReARMed**

Once that, we need to download a PSX BIOS, I let this url from [archive.org](https://archive.org/details/PlayStationBIOSFilesNAEUJP). I used it and It works well in my hardware with Linux.

The BIOS are:
-  scph5500 - 3.0 NTSC-J (1996-09-09)
-  scph5501 - 3.0 NTSC-U/C (1996-11-18)
-  scph5502 - 3.0 PAL (1997-01-06)

Put those BIOS in **retroarch/system**

Now start retroarch and you are ready to play!! :)
