#Conceptos básicos Python

Python es un lenguaje en el cual todo los datos son tomados como objetos, esto hace que tengan atributos y métodos a los cuales podemos acceder. Esto se abordara con más detalle a futuro.

En python podemos realizar nuestro proyectos haciendo uso de variables, pero, ¿Qué son las variables?

Las variables son un espacio reservado de memoria. Nos sirven para realizar operaciones entre ellas, interactuar con sistemas, validar operaciones, entre muchas otra funciones.
Podemos concebirlas como un baúl, el cual tiene un nombre, el modo de acceder a lo que hay dentro del baúl es usando ese nombre. Ejemplo:
```
python
x = 1
```
En este caso definimos una variable tipo int, los int son variables que contienen exclusivamente números enteros.

Si queremos llamarla vamos a tener que hacer referencia a ella como "x", dado a que es la forma en que la invocamos. SI queremos imprimirla en pantalla(terminal) podemos hacerlo a Trávez de la función "print":
```
python
print(x)
>>1
```

Como podemos observar al asignarle un valor a una letra cualquiera, la convertimos en una variable la cual tiene un valor especifico.

Pero, ¿Qué otros tipos de variables hay?

Tenemos varios tipos, cuales cumplen funciones diferentes:

float: Permite albergar números decimales con gran extensión y precisión.

str: Permite albergar cadenas de texto.

bool: Permite guardar variables booleanas, como True o False.

complex: Permite albergar números complejos.

Entre otros tipos de datos, estos son los esenciales. Python es un lenguaje el cual tiene tipado dinámico, no estático.
El tipado es una característica de los lenguaje de programación, se centra en la forma de declarar el tipo de variables.

El tipado estático es en donde el tipo está ligado a la variable, por lo mismo, normalmente al momento de declarar una variable debemos incluir explícitamente que tipo será.
Un ejemplo de lenguajes en los cuales pasa esto es en c++ o golang

El tipado Dinámico es en donde el tipo está ligado a el dato, por lo mismo, una variable antes definida con un tipo de dato puede tomar otro tipo de dato diferente.
Un ejemplo de lenguajes donde esto sucede es en Python.

Ahora, la forma en la que damos instrucciones se llaman declaraciones, estas declaraciones pueden ser de varios tipos, de hecho muchos. Vamos a ver algunas de estas:

Declaración de variables:

Tenemos dos formas principales, declarar la variable solamente con su valor, como:

x = 10
y = True
string = "Hello, world!"
...

Cuando usamos funciones como: int(), float(), str()
Al momento de declarar una variables, estamos dando un tipado a esas variables, estos tipados consumen tiempo para ser procesados, por lo cual es recomendar asignar valores directamente y tipar las variables cuando es estrictamente necesario.
 
x = int(10)
y = bool(True)
string = str("Hello, world!")
...

Operadores aritméticos:

Permiten realizar operaciones matemáticas básicas. Si queremos hacer operaciones más especifico es posible que debamos usar una librería externa, esto se explicara más a fondo en breve. Tenemos los siguientes operadores:

Suma: +
Resta: -
Multiplicación: *
División: /

También tenemos algunas operaciones básicas, como el modulo y la division que su resultado será únicamente una dato tipo int:

Modulo: %
División que retorna únicamente int: //


Operadores lógicos:

Tenemos tres tipos de operaciones lógicas:

not:
Retornara el inverso a un valor lógico. Si tenemos True y le aplicamos not, obtendremos un False, dado a que es el inverso de True.

not 	True 	= 	False

or:

Cuando tenemos un operador or, este priorizara el True, con esto me refiero a que este operador siempre retornara un True, si por lo menos hay uno.

True	 or 	True 	= 	True
False	 or 	True 	= 	True
True	 or 	False 	= 	True
False	 or 	False 	= 	False

and:
El operador and retornara True únicamente si los dos datos son True.

True	 and 	True 	= 	True
False	 and 	True 	= 	False
True	 and 	False 	= 	False
False	 and 	False 	= 	False


Constantes

Comentarios

Strings

Formatear Strings

Input

Control de flujo (if-else)

switch(match)


Ciclos

Funciones


variables globales

librerías

importar librerías

módulos

paquetes

manejo de errores



