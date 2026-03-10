
# Punto 4 — Comparación de rendimiento: Algoritmo de Euclides C & Haskell

## Descripción
En este ejercicio se implementó el Algoritmo de Euclides para calcular el máximo común divisor GCD de dos números en C y Haskell
El objetivo es comparar el rendimiento de ambos lenguajes midiendo el tiempo de ejecución al calcular:
GCD(123456789, 987654321)

## Algoritmo utilizado
El algoritmo de Euclides se basa en la siguiente propiedad:
GCD(a, b) = GCD(b, a mod b)
El proceso se repite hasta que b = 0 momento en el cual a contiene el resultado
Este algoritmo es eficiente porque reduce rápidamente el tamaño de los números.

## Ejecución del programa en C
Compilación:
gcc euclides.c -o euclides
Ejecución:
./euclides
Salida obtenida:
GCD(123456789,987654321) = 9
Tiempo C: 0.000004 segundos

## Ejecución del programa en Haskell
Ejecución:
runhaskell euclides.hs
"GCD(123456789,987654321) = 9"
"Tiempo Haskell: 0.000002608s"

## C
<img width="715" height="95" alt="image" src="https://github.com/user-attachments/assets/dbe2ae88-d576-4abd-b9da-ebdb328747ac" />

## Haskell
<img width="715" height="95" alt="image" src="https://github.com/user-attachments/assets/2af4d98c-18ec-414d-8c8c-724350e5d7eb" />


Ambos programas producen el mismo resultado 
GCD = 9
Los tiempos de ejecución son muy pequeños porque el algoritmo es altamente eficiente.

## Análisis de rendimiento
En esta ejecución particular, Haskell fue ligeramente más rápido que C
Esto puede ocurrir por varias razones:

* El tamaño del problema es muy pequeño, por lo que las diferencias reales de rendimiento son mínimas.
* El tiempo medido incluye pequeñas variaciones del sistema operativo.
* La implementación de recursión en Haskell puede ser optimizada por el compilador.
Sin embargo, en programas más grandes y con mayor carga computacional, C suele ser más rápido debido a que es un lenguaje de más bajo nivel

## Conclusión
Ambos lenguajes implementan correctamente el algoritmo de Euclides y obtienen el mismo resultado.
Las diferencias de tiempo observadas son muy pequeñas debido a que el algoritmo es rápido y el problema es pequeño. En aplicaciones de mayor escala, C suele ofrecer mejor rendimiento, mientras que Haskell proporciona una implementación más declarativa y concisa gracias a su enfoque funcional.

---
