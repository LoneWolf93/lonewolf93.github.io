---
title: "Plank no reconoce el entorno X11 y no se inicia"
layout: post
---

Para solucionar este error, en mi caso estoy en Openbox. Debemos modificar la variable `XDG_SESSION_TYPE` por defecto si hacemos en una terminal `echo $XDG_SESSION_TYPE` nos aparecera como resultado `tty` y por eso al ejecutar **Plank** tira el error:
```
[INFO 15:43:28.988037] [AbstractMain:229] Plank version: 0.11.2
[INFO 15:43:28.988103] [AbstractMain:230] Kernel version: 4.7.6-1-ARCH
[INFO 15:43:28.988143] [AbstractMain:231] GLib version: 2.50.1 (2.48.1)
[INFO 15:43:28.988187] [AbstractMain:234] GTK+ version: 3.22.1 (3.20.6)
[INFO 15:43:28.988223] [AbstractMain:237] Wnck version: 3.14.1
[INFO 15:43:28.988262] [AbstractMain:238] Cairo version: 1.14.6
[INFO 15:43:28.988301] [AbstractMain:239] Pango version: 1.40.3
[INFO 15:43:28.988337] [AbstractMain:241] + Cairo/Gtk+ HiDPI support enabled
[INFO 15:43:28.988374] [AbstractMain:247] + XInput Barriers support enabled
[WARN 15:43:28.988428] [Environment:161] XDG_SESSION_CLASS not set in this environment!
[CRITICAL 15:43:28.988486] [AbstractMain:257] Only X11 environments are supported.
```
Modificaremos la variable haciendo `export XDG_SESSION_TYPE=x11`.

## Página web consultada

Gracias a esta página web he dado con la solución: [bugs.launchpad.net](https://bugs.launchpad.net/plank/+bug/1811364)
