---
title: "Como saber que driver GPU estoy utilizando en estos momentos"
layout: post
---
Cuando instalé Debian y me pregunté ¿Cómo puedo ver que driver gráfico ha sido cargado?. Pues, con este sencillo comando podemos tener la información en varios segundos.

El comando en cuestión es: `lspci -nnk | grep -iA2 vga`

El resultado que nos da es el código y nombre del proveedor gráfico y el driver actualmente en uso.
