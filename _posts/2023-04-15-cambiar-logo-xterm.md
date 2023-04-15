---
title: "Cambiar el icono de la ventana de xterm"
layout: post
---
![](https://user-images.githubusercontent.com/16481438/232235478-5c3c4fca-f1d6-4d05-8bd8-615ea6ca98f5.png)

Reciente he cambiado el pack de iconos a papirus y la terminal xterm no cambiaba el icono pese a tener icono en papirus.

# Localizar la imagen

Para forzar a que aparezca el icono correcto tenemos que localizar la imagen, este suele estar en **/home/$USER[^1]/.icons/Papirus/16x16/apps**

El fichero es `utilities-x-terminal.svg`

# Editar la imagen

Una vez localizado con la ayuda de GIMP[^2] o [Convert SVG to XPM](https://convertio.co/es/svg-xpm/) debemos de convertir el fichero .svg a .xpm

Una vez hecho la conversion podemos guardarla donde queramos pero lo mas habitual es dejarlo en la ruta `/home/$USER/.icons/Papirus/16x16/apps` y le ponemos como nombre
xterm-modificado.xpm

# Editar fichero .Xresources

Abrimos un editor de texto y editamos el fichero .Xresources[^3]. Añadimos la sentencia `xterm*iconHint: /home/$USER/.icons/Papirus/16x16/apps/xterm-modificado` (Este debe de ir sin extension solo el nombre del fichero)

Guardamos el fichero .Xresources y lo cerramos, nuevamente en la terminal ejecutamos el comando `xrdb .Xresources` y cerramos la terminal.

Abrimos la terminal y ya podemos ver como el logo ha cambiado por el nuevo que hemos hecho. 

# Agradecimientos

Gracias a la web [https://dt.iki.fi/xterm-icon-tweaks](https://dt.iki.fi/xterm-icon-tweaks) he podido realizar este post y poder cambiar el logo a xterm. Esta misma web facilita unos iconos hecho por él [https://dt.iki.fi/stuff/blog/xterm_xpms.tar.gz](https://dt.iki.fi/stuff/blog/xterm_xpms.tar.gz)

# Notas a tener en cuenta
[^1]: Es nuestro nombre de usuario
[^2]: Programa de manipulación de imagenes digitales
[^3]: Fichero de configuración de xterm, debe de estar oculta en el directorio /home/usuario/
