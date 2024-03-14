---
title: "Plank no reconoce el entorno X11 y no se inicia"
layout: post
---

Para solucionar este error, en mi caso estoy en Openbox. Debemos modificar la variable `XDG_SESSION_TYPE` por defecto si hacemos en una terminal `echo $XDG_SESSION_TYPE` nos aparecera como resultado `tty` y por eso al ejecutar **Plank** tira el error `plank only X11 environments are supported openbox`. Modificaremos la variable haciendo `export XDG_SESSION_TYPE=x11`.

## Página web consultada

Gracias a esta página web he dado con la solución: [bugs.launchpad.net](https://bugs.launchpad.net/plank/+bug/1811364)
