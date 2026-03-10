# Punto 2 — ID

## Descripción

El programa lee una lista de cadenas desde un archivo de texto y determina si cada cadena pertenece o no al lenguaje de identificadores definido.
La ejecución del programa se realiza pasando el archivo de entrada como argumento desde la terminal.


# Definición del lenguaje

La expresión regular que define el lenguaje es:

[A-Za-z][A-Za-z0-9]*


Esto significa:

1. El identificador debe comenzar con una letra.
2. Después del primer carácter puede contener letras o números
3. Puede tener cero o más caracteres adicionales.

## Transiciones

(q0, letra) = q1
(q1, letra = q1
(q1, número) = q1

Si la cadena termina en q1 el identificador es aceptado

Si en cualquier momento aparece un carácter inválido, la cadena es rechazada

## Archivo de entrada

El archivo `entrada.txt` contiene las cadenas que serán evaluadas por el programa.

## Ejecución del programa
Para ejecutar el programa desde la terminal: python id.py entrada.txt

## Resultado esperado

Con el archivo de ejemplo, la salida será:

Mario : ACEPTA
08Mario : NO ACEPTA
hola30 : ACEPTA
prueba? : NO ACEPTA
_hola : NO ACEPTA
a : ACEPTA
w10 : ACEPTA

## Pruebas realizadas

Se realizaron pruebas con identificadores válidos e inválidos para verificar el correcto funcionamiento del AFD.
Las pruebas incluyen:

* Identificadores mínimos
* Identificadores con números
* Identificadores inválidos con caracteres especiales
* Identificadores que comienzan con números

# Conclusión

Se implementó un AGD capaz de validar identificadores definidos por la expresión regular [A-Za-z][A-Za-z0-9]*.
El programa analiza cada cadena proveniente de un archivo de texto y determina si cumple o no con las reglas del lenguaje. Esto permite verificar de manera automática la validez de identificadores según la definición establecida.
