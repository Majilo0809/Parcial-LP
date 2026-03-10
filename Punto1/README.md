# Punto 1 — AFD Ajedrez

## Descripción

En este ejercicio se definió un lenguaje para movimientos de ajedrez y se implementó un AFD en Python que permite verificar si una cadena pertenece o no a dicho lenguaje.
El programa recibe una cadena que representa un posible movimiento de ajedrez y determina si cumple la estructura definida por la expresión regular del lenguaje.

# Lenguaje definido

El lenguaje acepta movimientos con la siguiente estructura:
piezas + operador + pieza destino + posición
Ejemplo de cadenas válidas: p->k4  |  n->e5  |  kbpxqn  |  rb->n7
Donde:

* piezas: letras que representan piezas de ajedrez
* operador indica movimiento o captura
* pieza destino pieza hacia la que se mueve o captura
* posición una posición representada por un carácter alfanumérico

## Piezas permitidas
Las piezas válidas son:  p k q r b n

##Operadores permitidos
El lenguaje acepta dos operadores:
->   movimiento
x    captura

Ejemplo: p->k4  |   pnxk2
## Expresión regular

El lenguaje puede describirse mediante la siguiente expresión regular:

[pkqrbn]+(->|x)[pkqrbn][a-z0-9]

## AFD

El programa implementa un AFD utilizando estados, si la cadena termina en el estado 4, entonces el movimiento es válido.
En cualquier otro caso, el movimiento es rechazado

# Cómo ejecutar el programa

1. Abrir una terminal en la carpeta del archivo.

2. Ejecutar: python ajedrez_afd.py

Pruebas realizadas:
p->k4 : ACEPTA
p->K4 : NO ACEPTA
holaa : NO ACEPTA
kbpxqn : ACEPTA
n->e5 : NO ACEPTA
r->c3 : NO ACEPTA
r->b3 : ACEPTA
0809 : NO ACEPTA

# #Conclusión

El programa evalúa cada carácter de la cadena y realiza transiciones entre estados hasta determinar si la cadena pertenece o no al lenguaje definido por la expresión regular.
