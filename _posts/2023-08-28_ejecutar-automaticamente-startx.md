# Ejecutar automáticamente startx

Si queremos ejecutar automaticamente `startx` necesitamos crear un fichero en el HOME del usuario, la ruta es /home/nombre-usuario

El fichero que tenemos que crear se debe llamar **.bash_profile** este fichero debe contener las siguientes lineas de código en BASH.

```bash
if [[ -z $DISPLAY ]] && [[ $(tty) = /dev/tty1 ]]; then
  startx
fi
```

Esto lo que hará es que al hacer sesion sin tener un GUI para iniciar sesion startx se ejecutara de manera automatica al iniciar sesion de manera en consola o TTY.
