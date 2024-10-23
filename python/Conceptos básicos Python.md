> # Conceptos básicos Python

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
# Ejemplo de operaciones con variables tipo complex


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

>- ##  Declaración de variables:

Tenemos dos formas principales, declarar la variable solamente con su valor, como:
```
# Ejemplo de declaración de variable
x = 10
y = True
string = "Hello, world!"
```

Cuando usamos funciones como: int(), float(), str()
Al momento de declarar una variables, estamos dando un tipado a esas variables, estos tipados consumen tiempo para ser procesados, por lo cual es recomendar asignar valores directamente y tipar las variables cuando es estrictamente necesario.

```
# Ejemplo de asignación de tipo

x = int(10)
y = bool(True)
string = str("Hello, world!")
```
## Fundición de tipos

Cuando declaramos una variable en python, esta normalmente se le declara con un tipo, ya sea explicitamente o implicitamente:

```
# Ejemplo de declaración explicita e implicita

# declaración de tipo explicita
num = int(5)

# declaración de tipo implicita
num = 5
```
Como notamos en los dos ejemplos, cuando hacemos un declaración explicita, asignamos un tipo de variable usando las funciones integradas de python. Sin embargo, podemos usar esta caracteristica para redeclarar el tipo de una variable. Un ejemplo es cuando tenemos una entrada númerica de el usuario, esta entrada es un string por defecto, por lo que si queremos usarla para realizar calculos matemáticos no podremos hacerlo.
Para esto usaremos la función de tipos:
```
# Ejemplo de fundición

num = input('Ingrese un número')
print(type(num).__name__)
>> str

num = int(input('Ingrese un número'))
print(type(num).__name__)
>> int
```
Ahora, tenemos dos tipos de funciones de tipo.
### Fundición implicita
Se presenta cuando una variable toma un valor ya existente, esta tomara automaticamente el tipo que tenga la variable. Esta es una caracteristica de python, resulta util porque nos evita tener que declarar cada cambio, más sin embargo, no nos permite tener control de cuando suceden estas. Un ejemplo es:

```
# Ejemplo de fundición implicita

# Variable tipo int
num = 5
# Variable con tipo de la variable num
nuevo_num = num

print(type(num).__name__, type(nuevo_num).__name__)
>> int, int
```

### Fundición explicita
Se presenta cuando a tráves de las funciones integradas de python, forzamos el cambio o la fundición de tipo. Un ejemplo sería:
```
# Ejemplo de fundición explicita

num = float(input('Digite el valor de una libra de arroz')
print(type(num).__name__)
>> float
```

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
Los strings son cadenas o arreglos de caracteres. Por lo mismo, podemos acceder a cada uno de los caracteres de un string como si fuera un arreglo:
```
ejemplo_string = 'Hola soy un ejemplo'
print(ejemplo_string[2])
>>l
```
También como en los arreglos, podemos acceder a rango de letras:
```
ejemplo_string = 'Hola soy un ejemplo'
print(ejemplo_string[2:6])
>>la s
```
En los strings los espacios también son caracteres. Cuando establecemos un rango funcionara de la siguiente forma: [incio, final -1, paso], esto nos explica porque solo llegamos hasta s en el ejemplo anterior, ya que el paso final no se incluye a sí mismo. 
El paso indica la cada cuantos caracteres contaremosm por ejemplo:
```
ejemplo_string = 'Hola soy un ejemplo'
print(ejemplo_string[0:8:2])
>>Hl o
```
Como podemos observar, se toman los caracteres cada dos pasos en el rango establecido.

## Formatear Strings
El formatear strings es una forma de concatenar variables en nuestros strings...

## Función Input

La función input es una función integrada en python, que nos permite que el usuario interactue con el script e ingrese valores a tráves de la terminal. Debemos tener en cuenta que los valores ingresados en la terminal serán strings, por lo que si queremos cambiar esto debemos hacer una fundición de tipo explicita (esto se explica más a fondo más adelante).
```
edad = input('Ingrese su edad')
print(type(edad).__name__)
>>str
```
Ejemplo con fundición de tipo explicita:
```
edad = int(input('Ingrese su edad'))
print(type(edad).__name__)
>>int
```

## Estructuras de datos en python
scoping
Es un concepto en python el cual nos permite tener más control sobre los elemento de nuestro código. Podemos verlo como una especie de encapsulamiento. El scoping nos permite declarar cuatro tipos de variables que tendrán un nivel de alcance diferente, las cuales son:
>- ### Local
>- ### Global
>- ### Encerrado (enclosing)
>- ### Incorporado (buil-in)

### Niveles de ámbito en python

## Listas, tuplas, sets y diccionarios

### Listas
split
join
### Tuplas
### Sets
### diccionarios

## Control de flujo (if-else)

## Switch(match)

## Ciclos

## Funciones
### *args
### **kwargs

## variables globales

## librerías

## Importar librerías

## Módulos

## Paquetes

## Manejo de errores (exepciones)

En python, como en otros lenguajes, tenemos errores, dichos errores se conocen como excepciones. Estas excepciones son diversas y podemos tratar de depurarlas o "adelantarnos" a su posible aparición. Esto lo podemos manejar con las siguientes declaraciones:

```
def division(a, b):
  try:
      a / b
  except:
    print('Algo anda mal, revisa la operación')
```
En el anterior ejemplo vimos una función, la cual en caso tal de no funcionar, imprimimos en pantalla "Algo anda mal, revisa la operación". Esta es una forma de capturar excepciones, pero, podemos ser mucho más especificos, ejemplo es cuando tenemos una división por cero:
```
def division(a, b):
  try:
      a / b
  except ZeroDivisionError as e:
    print(f'Algo anda mal, {e}')
```
El anterior ejemplo nos permite capturar un error especifico, que es qque en caso de dividir por 0, imprimira en pantalla "Algo anda mal, ZeroDivisionError", indicandole al usuario el error que está cometiendo, permitiendo que lo corrija más facilmente.

También podemos encadenar erorres, en caso de que un error previsto no suceda, sino otro.
```
def division(a, b):
  try:
      a / b
  except ZeroDivisionError as e:
    print(f'Algo anda mal, {e}')
  except Exception as e:
    print(f'Algo anda mal, {e}')
```
En este ejemplo nos mostrar el error que estamos teniendo, independientemenete si es una división entre cero o no. Además, podemos incluir al final la sentencia else para indicar que queremos hacer en caso de no haber excepciones:
```
def division(a, b):
  try:
      a / b
  except ZeroDivisionError as e:
    print(f'Algo anda mal, {e}')
  except Exception as e:
    print(f'Algo anda mal, {e}')
  else:
    return a/b
```
Aveces está sentencía es innecesaria ya que try cumple la misma función, pero aveces puede ser util, en diversas situaciones.

## Manejo de archivos

Con open la forma predeterminada de abrir el archivo es read(r) o leer
Añadir close() al final
>- r
>- r+
>- a -  append
>- w -  write

rb
rb+
ab
wb

archivo = open(file=direccción, mode=a)

### Creación de archivos

with open('file.txt', 'w') as file:
  file.write('Hola soy un nuevo archivo')

with open('file.txt' ,'a') as file:
  file.writelines(['\nSoy nueva linea 1', '\nSoy nueva linea 2'])

try:

except FileNotfoundError:

### Lectura de archivos

Cambiar a archivo el file, añadir ejemplos de todos los read

read()  --> lee todo el archivo, con un argumetno imprime hasta el numero de caracteres especificado 
read(44) imprime hasta ese caracter
readline() --> puede pasar argumento para leer caracteres
readlines() --> retorna lista de cadenas, puede añadirse a una variable y poder iterar en el

with open('file.txt', 'r') as file:
  data = file.readlines()

  for linea in data:
    print(linea)

Se puede hacer de forma abreviada, cuando se abre como read, este retornara el archivo como lista por defecto, permitiendonos:

with open('file.txt', 'r') as file:
  for linea in file:
    print(linea)
  file.close()

#### Ruta absoluta
incluye directorio C
#### Ruta relativa
Relativa al directorio actual

./sample.txt


variable igual a archivo 

f = open('sample.txt', 'r')
f.close()

```
def read_file(file_name):
    """ Reads in a file.

    [IMPLEMENT ME]
        1. Open and read the given file into a variable using the File read()
           function
        2. Print the contents of the file
        3. Return the contents of the file

    Args:
        file_name: the name of the file to be read

    Returns:
        string: contents of the given file.
    """
    ### WRITE SOLUTION HERE
    try:
        file = open(file_name, 'r')
    except FileNotFoundError as e:
        print(e)
    content = file.read()
    print(content)
    return content


def read_file_into_list(file_name):
    """ Reads in a file and stores each line as an element in a list

    [IMPLEMENT ME]
        1. Open the given file
        2. Read the file line by line and append each line to a list
        3. Return the list

    Args:
        file_name: the name of the file to be read

    Returns:
        list: a list where each element is a line in the file.
    """
    ### WRITE SOLUTION HERE
    try:
        lines =[]
        with open(file_name) as file:
            for line in file:
                lines.append(line)
    except FileNotFoundError as e:
        print(e)
    return lines


def write_first_line_to_file(file_contents, output_filename):
    """ Writes the first line of a string to a file.

    [IMPLEMENT ME]
        1. Get the first line of file_contents
        2. Use the File write() function to write the first line into a file
           with the name from output_filename

        We determine the first line to be everything in a string before the
        first newline ('\n') character.

    Args:
        file_contents: string to be split and written into output file
        output_filename: the name of the file to be written to
    """
    ### WRITE SOLUTION HERE
    try:
        line = file_contents.split('\n')[0]
    except FileNotFoundError as e:
        print(e)

    with open(output_filename, 'w') as file:
        file.writelines(line)




def read_even_numbered_lines(file_name):
    """ Reads in the even numbered lines of a file

    [IMPLEMENT ME]
        1. Open and read the given file into a variable
        2. Read the file line-by-line and add the even-numbered lines to a list
        3. Return the list

    Args:
        file_name: the name of the file to be read

    Returns:
        list: a list of the even-numbered lines of the file
    """
    ### WRITE SOLUTION HERE
    even_numbered = []
    try:
        file_content = open(file_name).readlines()
    except FileNotFoundError as e:
        print(e)
    except Exception as e:
        print(e)
    for i in range(1, len(file_content), 2):
        even_numbered.append(file_content[i])
    return even_numbered


def read_file_in_reverse(file_name):
    """ Reads a file and returns a list of the lines in reverse order

    [IMPLEMENT ME]
        1. Open and read the given file into a variable
        2. Read the file line-by-line and store the lines in a list in reverse order
        3. Print the list
        4. Return the list

    Args:
        file_name: the name of the file to be read

    Returns:
        list: list of the lines of the file in reverse order.
    """
    ### WRITE SOLUTION HERE
    lines = []
    try:
        with open(file_name, 'r') as file:
            for line in file:
                lines.append(line)
    except FileNotFoundError as e:
        print(e)
    reverse_file = lines[::-1]
    return reverse_file


'''
Here are some sample commands to help you run/test your implementations.
Feel free to uncomment/modify/add to them as you wish.
'''
def main():

    file_contents = read_file("sampletext.txt")
    #print(read_file_into_list("sampletext.txt"))
    #write_first_line_to_file(file_contents, "online.txt")
    #print(read_even_numbered_lines("sampletext.txt"))
    #print(read_file_in_reverse("sampletext.txt"))

if __name__ == "__main__":
    main()
```
