---
title: "Dunst"
layout: post
---
# Que es Dunst?

Es un gestor de notificaciones que nos permite dar información de alertas de diferentes programa como por ejemplo cuando entra un mensaje de correo nuevo en Thunderbird, comienza a reproducir una canción en Audacious, aumentamos el volumen de nuestros altavoces, etc.

# Instalación

Dunst ya viene en las principales distribuciones como Debian , Arch Linux, Manjaro, Ubuntu, Fedora, etc.

Yo lo haré desde una distribucion Debian-like[^1]. Tenemos que abrir una terminal y ejecutar el comando `apt install dunst`

Con esto ya lo tenemos instalado, ahora veremos como podemos configurarlo.

# Configuración

Dentro de `/home/$USER/.config` deberia de haber una carpeta llamada `dunst` si no existe debemos crearla y dentro creamos un texto en blanco llamado `dunstrc`

Ahora toca pegar la información por defecto. Podemos obtenerla desde el propio repositorio del proyecto dunst haciendo [clic aqui](https://github.com/dunst-project/dunst/blob/master/dunstrc).

Como alternativa si algun dia deja de existir dicho repositorio lo facilito en este mismo post haciendo [clic aqui](https://github.com/LoneWolf93/lonewolf93.github.io/blob/master/_config-files-by-default/dunstrc) o [este por si falla](https://paste.debian.net/hidden/429a39c4/).

## Información a tener en cuenta

Dentro del fichero `dunstrc` podemos cambiar el color de fondo, estilo de la fuente, tamaño de la notificacion, etc.

### Cambiar la fuente predeterminada
Para cambiar la fuente debemos dirigirnos a la linea 129 o en su defecto `font = Nombre de la fuente [ESPACIO] tamaño de letra`, ejemplo, `font = Terminus 12`

### Cambiar el color de las notificaciones

A partir de la linea 317 tenemos lo que son el nivel de la notificación, es decir, una notificación puede tener un estado de los 3 posibles:

- LOW
- NORMAL
- CRITICAL

Normalmente el que más se utiliza es el LOW o NORMAL, podemos cambiar el color donde corresponde como:

- Background
- Foreground

### Poner tiempo de vision a las notificaciones

Tambien tenemos el timeout que este espera un numero, este numero es el tiempo que estara activa la notificación visible en el escritorio.

### Cambiar el icono predeterminador

Tambien es posible cambiar el icono que aparece por defecto, para poder cambiarlo debemos de añadir / modificar el parametro:

`icon = ruta_del_icono`

### Añadir reglas

Por ultimo tenemos lo que son las reglas. Podemos aplicar condiciones para las aplicaciones, es decir, modificar el compartamiento de la notificacion para según que aplicación.

Ejemplo:

```
[musicplayer]
appname = Audacious
history_ignore = true
```

```
[volume]
appname = pnmixer
new_icon = /home/albert/.config/dunst/audio-x-generic.svg
format="Volumen al %p"
history_ignore = true
timeout = 2
```

```
[programp2p]
appname = aMule
new_icon = /home/albert/.config/dunst/information-bell.svg
timeout = 10
```


En los tres ejemplos vistos arriba tenemos tres reglas que como valor importante es el `appname` este tendra que ser igual al que esta en `/usr/share/applications/X.desktop` donde X va el nombre de la aplicación. Dentro del fichero tiene que ser el mismo que el del parámetro `Name=`


# Conclusion

Este gestor de notificaciones es inmenso, tiene infinidad de configuraciones, en este articulo he comentado muy superficialmente pero tiene muchas cosas más.

Pruebalo y no querras cambiarlo por nada.

[^1]: Es una manera de decir distribuciones basadas en Debian o paqueteria DEB

un entorno que no viene predeterminado una opción muy buena es [Dunst](https://dunst-project.org/)

---
# fuentes consultadas

![https://linuxconfig.org/get-better-notifications-in-your-wm-with-dunst](https://linuxconfig.org/get-better-notifications-in-your-wm-with-dunst)

![https://dunst-project.org/](https://dunst-project.org/)

![https://github.com/dunst-project/dunst](https://github.com/dunst-project/dunst)

![https://wiki.archlinux.org/title/Dunst](https://wiki.archlinux.org/title/Dunst)

![https://atareao.es/tutorial/bspwm/dunst-las-notificaciones-en-bspwm/](https://atareao.es/tutorial/bspwm/dunst-las-notificaciones-en-bspwm/)

![https://www.addictivetips.com/ubuntu-linux-tips/set-up-better-system-notifications-on-linux-with-dunst/](https://www.addictivetips.com/ubuntu-linux-tips/set-up-better-system-notifications-on-linux-with-dunst/)

![https://github.com/dunst-project/dunst/blob/master/dunstrc](https://github.com/dunst-project/dunst/blob/master/dunstrc)

![https://www.youtube.com/watch?v=XWlbaERuDP4](https://www.youtube.com/watch?v=XWlbaERuDP4)

[https://manpages.ubuntu.com/manpages/jammy/en/man1/dunst.1.html](https://manpages.ubuntu.com/manpages/jammy/en/man1/dunst.1.html)
