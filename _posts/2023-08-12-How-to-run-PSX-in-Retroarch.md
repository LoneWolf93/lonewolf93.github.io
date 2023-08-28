---
title: "Ejecutar PSX en Retroarch en Debian 12"
layout: post
---

Debes descargarte el appimage desde [https://buildbot.libretro.com/nightly/linux/x86_64/RetroArch.7z](https://buildbot.libretro.com/nightly/linux/x86_64/RetroArch.7z).

Una vez descargado tienes que aplicar los permisos en el appimage haciendo clic derecho > propiedades > ejecutar solo el propietario.

Dentro del sistema Retroarch tienes que descargarte el nucelo de la PSX, segun he visto por Reddit hay dos nucleos muy buenos:
-  Para equipos x86 or x64: **Beetle PSX HW**
-  Para Android o basado en ARM: **PCSX ReARMed**

Una vez hecho esto de momento no podemos ejecutar los juegos porque nos pedira una Bios, he podemos sacar Bios utilizables en [archive.org](https://archive.org/details/PlayStationBIOSFilesNAEUJP).

Las BIOS son:
-  scph5500 - 3.0 NTSC-J (1996-09-09)
-  scph5501 - 3.0 NTSC-U/C (1996-11-18)
-  scph5502 - 3.0 PAL (1997-01-06)

Copia las Bios en **retroarch/system**

Ejecuta Retroarch y viciate durante horas!! :)
