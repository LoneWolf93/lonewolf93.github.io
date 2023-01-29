---
title: "Prevenir el screen tearing en pantallas externas"
layout: post
---
[Screen tearing](https://es.wikipedia.org/wiki/Tearing) puede aparecer cuando utilizas el driver/modulo kernel amdgpu en las AMD Renoir u otras.

Con unos simples comando y un posterior reinicio podremos arreglar este molesto error.

Se debe utilizar el comando de shell xrandr[^1]

1. `xrandr --verbose | grep TearFree`
2. `xrandr --output HDMI-A-0 --set TearFree on`

## Hacer persistente el tearfree

Para hacer persitente el cambio se tiene que crear un fichero y posteriormente un reinicio o reiniciando el servidor X[^2]

1. Creamos un fichero llamado 20-amdgpu.conf y lo alojamos en /etc/X11/xorg.conf.d/

La ruta debe quedar: `/etc/X11/xorg.conf.d/20-amdgpu.conf`
   
2. El contenido del fichero debe ser el siguiente:
  
  ```
  Section "Device"
      Identifier "AMD Graphics"
      Driver "amdgpu"
      Option "TearFree" "true"
   EndSection
  ```
Me he basado en la web [Oficial de Debian](https://wiki.debian.org/AtiHowTo#Preventing_screen_tearing)

[^1]: Se puede descargar del repositorio de debian a traves del enlace [Paquete xrandr para instalarlo en debian 11 bullseye](https://packages.debian.org/bullseye/x11-xserver-utils)
[^2]: El servidor X se refiere a las ventanas, xorg. Sale mas comodo reiniciar el equipo.
