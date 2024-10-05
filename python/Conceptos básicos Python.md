# Conceptos básicos Python

Python es un lenguaje en el cual todo los datos son tomados como objetos, esto hace que tengan atributos y métodos a los cuales podemos acceder. Esto se abordara con más detalle a futuro.

En python podemos realizar nuestro proyectos haciendo uso de variables, pero, ¿Qué son las variables?

Las variables son un espacio reservado de memoria. Nos sirven para realizar operaciones entre ellas, interactuar con sistemas, validar operaciones, entre muchas otra funciones.
Podemos concebirlas como un baúl, el cual tiene un nombre, el modo de acceder a lo que hay dentro del baúl es usando ese nombre. Python tiene tipado dinamico, aspecto que veremos más a fondo en breve, por el momento solo debes de saber que una variable puede cambiar de tipo constantemetne y el compilador lo asignara automaticamente. Ejemplo:
```
#  Ejemplo de declaración de variable tipo entero(int)

x = 1
# Verificamos el tipo de variable
print(type(x).__name__)
>>'int'

# Ejemplo de declaración tipo string

# Asignamos un tipo diferente  a la variable
x = str(x)
# Verificamos el tipo
print(type(x).__name__)
>>'str'
```

En este caso definimos una variable tipo int, los int son variables que contienen exclusivamente números enteros. Luego, reasignamos el tipo de variable, ahora es string, una variable tipo cadena la cual es un arreglo de caracteres a los cuales podemos acceder de manera independiente. En breve veremos que es una lista.

Si queremos llamarla vamos a tener que hacer referencia a ella como "x", dado a que es la forma en que la invocamos. Si queremos imprimirla en pantalla(terminal) podemos hacerlo a Trávez de la función "print":
```
# Ejemplo de uso de la función para imprimir en pantalla(print)

print(x)
>>1
```

"print" es una funcion integrada de python, es una palabra reservada, por lo mismo no podremos usarla para definir variables. Como podemos observar al asignarle un valor a una letra cualquiera, la convertimos en una variable la cual tiene un valor especifico.

Pero, ¿Qué otros tipos de variables hay?. Hemos visto dos tipos "int"(enteros) y "str"(string), más sin embargo también tenemos otros varios tipos:

- int: Permite albergar números enteros. Su palabra reservada es "int". A continuación un ejemplo de uso:
  ```
  # Ejemplo de declaración de variable tipo int
  
  int_var = 10
  print(type(int_var).__name__)
  >>int
  ```

- float: Permite albergar números decimales con gran extensión y precisión. Su palabra reservada es "float". A continuación un ejemplo de uso:
  ```
  # Ejemplo de declaración de variable tipo float
  
  # Asignamos un valor decimal
  float_var = 3.14
  print(type(float_var).__name__)
  >> float

  # AHora pasamos de int a float

  x = 4
  print(type(float_var).__name__)
  >> int

  x = float(4)
  print(type(float_var).__name__)
  >> float

  # Podemos almacenar decimales con alta presición
  x = 0.123412
  print(float_var)
  >> 0.123412
  ```

- string: Permite albergar cadenas de texto, permitiendo acceder a cada uno de sus caracteres de forma independiente. Su palabra reservada es "str". A continuación un ejemplo de uso:
  ```
  # Ejemplo de declaración de variable tipo string
  
  string_var = 'hola'
  # Imprimimos toda la cadena
  print(string_var)
  >>hola

  # Imprimimos un caracter especifico de la cadena
  print(string_var[0])
  >>h

  # Imprimimos un rango de la cadena
  print(string_var[0:1)
  >>ho
  ```

- boolean: Permite guardar variables booleanas, como True o False. Este tipo de variables son impresendibles para  verificar tipos de entrada, validaciones de declaraciones lógicas, entre otras funciones imprecindibles. Tiene principalmente dos valore: "True" y "False", las cuales traducen literalmente "Verdadero" y "Falso". La palabra reservada para este tipo de variable es "bool". A continuación un ejemplo de uso:
```
# Ejemplo de declaración de variable tipo bool
# Verdadero 
bool_var = True
print(type(bool_var).__name__)
>>bool

# Falso
bool_var = False
print(type(bool_var).__name__)

```




- complejos: Permite albergar números complejos, estos se definen usando j. Su tipo de variable es "complex", igual que su variable reservada. Y permite varias operaciones con números complejos. A continuación ejemplos de uso:

```
# Ejemplo de declaración de variable tipo complex


z1 = 4 +5j
print(type(z1).__name__)
>> complex

# operaciones con números complejos

z2 = 3 + 4j

print(z1+z2)
print(z1-z2)
print(z1*z2)
print(z1/z2)
>> 7 + 9j
>> 1 + 9j
>> -8 + 31j
>> 1.28 - 0.04j

# Podemos extraer también su parte real e imaginaria

z3 = z1 +z2

print(z3.real)
print(z3.imag)
>> 7
>> 9


```
  
# Tipado Dinamico en python

Python es un lenguaje el cual tiene tipado dinámico, no estático. El tipado es una característica de los lenguaje de programación, se centra en la forma de declarar el tipo de variables.

El tipado estático es en donde el tipo está ligado a la variable, por lo mismo, normalmente al momento de declarar una variable debemos incluir explícitamente que tipo será. Un ejemplo de lenguajes en los cuales pasa esto es en c++ o golang

El tipado Dinámico es en donde el tipo está ligado a el dato, por lo mismo, una variable antes definida con un tipo de dato puede tomar otro tipo de dato diferente. Un ejemplo de lenguajes donde esto sucede es en Python.

Ahora, la forma en la que damos instrucciones se llaman declaraciones, las hemos estado usando al momento de definir variables o imprimir en pantalla. Estas declaraciones pueden ser de varios tipos, de hecho muchos. Vamos a ver algunas de estas:

##  Declaración de variables:

Tenemos dos formas principales, declarar la variable solamente con su valor, como:
```
python
x = 10
y = True
string = "Hello, world!"
```

Cuando usamos funciones como: int(), float(), str()
Al momento de declarar una variables, estamos dando un tipado a esas variables, estos tipados consumen tiempo para ser procesados, por lo cual es recomendar asignar valores directamente y tipar las variables cuando es estrictamente necesario.

```
python
x = int(10)
y = bool(True)
string = str("Hello, world!")
```
## Fundición de tipos

### Fundición implicita

### Fundición explicita


## Operadores aritméticos:

Permiten realizar operaciones matemáticas básicas. Si queremos hacer operaciones más especifico es posible que debamos usar una librería externa, esto se explicara más a fondo en breve. Tenemos los siguientes operadores:

````
Suma: +
Resta: -
Multiplicación: *
División: /
````
También tenemos algunas operaciones básicas, como el modulo y la division que su resultado será únicamente una dato tipo int:
```
Modulo: %
División que retorna únicamente int: //
```

## Operadores lógicos:

Tenemos tres tipos de operaciones lógicas:

### not:
Retornara el inverso a un valor lógico. Si tenemos True y le aplicamos not, obtendremos un False, dado a que es el inverso de True.
```
python
not 	True 	= 	False
```

### or:

Cuando tenemos un operador or, este priorizara el True, con esto me refiero a que este operador siempre retornara un True, si por lo menos hay uno.
```
True	 or 	True 	= 	True
False	 or 	True 	= 	True
True	 or 	False 	= 	True
False	 or 	False 	= 	False
```

### and:
El operador and retornara True únicamente si los dos datos son True.
```
True	 and 	True 	= 	True
False	 and 	True 	= 	False
True	 and 	False 	= 	False
False	 and 	False 	= 	False
```

## Constantes

Las constantes son un tipo de dato que no modificaremos en la ejecución de nuestro programa. Se suele asigrnar a direcciones o rutas especificas, numeros constantes que seguiremos usando. Este tipo de notación se hace por convención, dado a que python no tiene una palabra clave o reservada para definir esto.

Las declaramos en mayusculas en su totalidad:
```
CONSTANT_VAR = 5
```

Las listas tambien pueden ser constantes, aunque normalemente se suelen usar tuplas en su lugar.

## Comentarios

Los comentarios son una forma de "documentar" o proporcionar información sobre funciones de nuestro código, dentro del mismo.
Se declaran con "#" para iniciar una linea o parte de ella, apartir de esto el compilador no prosesara ese fragmento de codigo.
Python como tal no tiene forma de declarar bloques de código, pero aveces son reemplazados con estas dos opciones:

```
# Linea 1
# Linea 2
# LInea 3

"""
Linea 1
LInea 2
Linea 3
"""

'''
Linea 1
LInea 2
Linea 3
'''
```
Hay ciertar reglas opcionales que brindan una buena legebilidad a nuestro código, este conjunto de reglas se llaman el "PEP 8".
Y puedes consultarlas en: https://pep8.org/
## Strings

## Formatear Strings

## Función Input

## Listas, tuplas, sets y diccionarios

### Listas
### Tuplas
### Sets
### diccionarios

## Control de flujo (if-else)

## Switch(match)

## Ciclos

## Funciones

## variables globales

## librerías

## Importar librerías

## Módulos

## Paquetes

## Manejo de errores



