# Punto 3- Raíz cuadrada usando Newton-Raphson

## Descripción
En este ejercicio se implementó un programa en C utilizando Flex y Bison para calcular la raíz cuadrada de un número usando el método de Newton-Raphson.
El programa lee las instrucciones desde un archivo de texto y calcula la raíz cuadrada de cada número indicado.

## Método utilizado

Se utiliza la iteración de Newton-Raphson para aproximar la raíz cuadrada de un número (S)
El proceso se repite hasta que el error sea muy pequeño.

## Formato de entrada
Las operaciones se escriben en el archivo entrada.txt con el formato:

sqrt numero

Ejemplo:
sqrt 1
sqrt 12

## Compilación

Generar el parser con Bison:
bison -d calc.y

Generar el lexer con Flex:
flex calc.l
Compilar el programa:
gcc calc.tab.c lex.yy.c main.c -lm -o calc

## EjecuciónEjecutar el programa indicando el archivo de entrada:
./calc entrada.txt

## Ejemplo de salida
entrada.txt contiene:

sqrt 1
sqrt 2
sqrt 3

La salida será:
sqrt(1.000000) = 1.000000
sqrt(2.000000) = 1.414214
sqrt(3.000000) = 1.732051
