---
title: "xterm esa vieja gloria llamada terminal"
layout: post
---
# XTERM
A dia de hoy tenemos decenas de terminales para Linux:

- Alacritty
- Kitty
- Konsole
- GNOME Terminal
- rxvt

He puesto solo unos pocos pero hay tal cantidad de terminales que no sabemos cual elegir, normalmente los usuarios del hogar escogen el que viene por defecto, si estas en Xfce pues tocara Xfce Terminal, KDE sera Konsole y así para su respectivo entorno de escritorio.

Personalmente he probado unos pocos pero siempre acabo en uno de los más básicos y antiguos que hay, este es XTERM.

Para saber lo básico de este terminal X debemos viajar al pasado. Este fue creado en 1984 de la mano Mark Vandevoorde y del desarrollador Thomas Dickey y a dia de hoy continua actualizandose, de locos!. Se dice que en mas de 30 años solo ha tenido una vulnerabilidad y se arreglo rápidamente.

# Ventajas y desventajas

Que hace que XTERM sea muy bueno. Sus ventajas es la sencillez y velocidad de respuesta que tiene, para estaciones de trabajo con pocos recursos es una delicia. Este terminal lo podemos considerar veterano, esto quiere decir que tiene una estabilidad brutal.

Por otro lado, sus desventajas pueden ser el aspecto visual, quizas de primeras o como lo dicen en inglés «out of the box» que en español viene siendo «listo para usar» se puede ver un poco anticuado.

![](https://linuxcommand.org/images/adventure_powerterm_rxvt_default.png)

La imagen superior es el aspecto cuando lo iniciamos por primera vez, se ve realmente feo pero con la ayuda del fichero .Xresources le podemos dar un toque mas a nuestro gusto. Yo le di mi toque y lo deje así.

![](https://raw.githubusercontent.com/LoneWolf93/lonewolf93.github.io/master/_images/xterm-images/2023-03-12_646x409_17%3A02%3A40_scrot-window-active.png)

# Fichero de configuración

Mi fichero de configuración es muy básico. Soy amante del minimalismo.

```
*.background:   #151515
*.cursorColor:  #d7d0c7

! black
*.color0:       #101010
*.color8:       #404040

! red
*.color1:       #e84f4f
*.color9:       #d23d3d

! green
*.color2:       #b8d68c
*.color10:      #a0cf5d

! yellow
*.color3:       #e1aa5d
*.color11:      #f39d21

! blue
*.color4:       #7dc1cf
*.color12:      #4e9fb1

! magenta
*.color5:       #9b64fb
*.color13:      #8542ff

! cyan
*.color6:       #6d878d
*.color14:      #42717b

! white
*.color7:       #dddddd
*.color15:      #dddddd

! size font
xterm*faceName: Terminus
xterm*faceSize: 12
```

# Conclusión

Podemos hablar que XTERM no es para todo el mundo, sobretodo si la persona acaba de aterrizar. Para otros quizás lo ven anticuado y con falta de caracteristicas, pero yo lo veo para lo que es un terminal X, ligero y minimalista para trabajar en él.
