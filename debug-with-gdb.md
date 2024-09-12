# Depuración con gdb

Esta información ha sido adaptada del GDB User Manual [[1]](http://www.google.com/url?q=http%3A%2F%2Fsourceware.org%2Fgdb%2Fdocumentation%2F&sa=D&sntz=1&usg=AFQjCNGBDnHmXjWMxtKD5b9nKkGqQtQK8g)

* Antes de depurar, es necesario compilar con la opción \-g. Por ejemplo: 

```shell 
gfortran -g -o a.out hola.f90
```

* Luego se lanza el depurador indicando el nombre del ejecutable:

```shell 
gdb ./a.out
```

Esta tabla resume una serie de comandos útiles.

| *Acción* | *Comando*  |
| :---- | :---- |
| **list:** ver el código (10 líneas centradas en la línea 5\)  | `l hola.f90:5`  |
| **breakpoint:** poner un punto de interrupción en la línea 8  | `b 8`  |
| **run:** lanzar el ejecutable (desde el principio)  | `r`  |
| **continue:** continuar la ejecución (tras llegar a un punto de  interrupción)  | `c` |
| **step:** ejecutar la siguiente sentencia (entrando en los procedimientos)  | `s` |
| **next:** ejecutar la siguiente sentencia (sin entrar en las funciones)  | `n` |
| **print:** imprimir en pantalla el valor de la variable x     | `p x` |
| **quit:** salir del GDB             | `q` |

              
