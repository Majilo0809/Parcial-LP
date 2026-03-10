# Punto 5 - Serie de Maclaurin e^x

## Descripción
En este ejercicio se implementó un programa que calcula una aproximación de e^x utilizando los primeros n términos de la serie de Maclaurin
El programa lee expresiones desde un archivo de texto y calcula el resultado para cada una.

## Formato de entrada
Las expresiones deben escribirse en el archivo entrada.txt con el siguiente formato:

exp(x,n)
donde:
- x -> valor de la variable
- n -> número de términos de la serie

## Compilación
Primero se genera el parser con ANTLR:
antlr4 Maclaurin.g4

Luego se compilan los archivos Java:
javac *.java

## Ejecución
Para ejecutar el programa:
java Main
## Ejemplo de salida

La entrada.txt` contiene:

exp(3,10)
exp(2,5)
exp(30,1)

La salida será similar a:
Resultado aproximado de e^3.0 = 20.063392857142855
Resultado aproximado de e^2.0 = 7.0
Resultado aproximado de e^30.0 = 1.0

