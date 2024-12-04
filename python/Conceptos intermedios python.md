## List comprehension

### Comprensión de lista 
[ <expression> for x in <sequence> if <condition>] 

### Comprensión de diccionario 
dict = { key:value for key, value in <sequence> if <condition> } 
months = ["Jan", "Feb", "Mar", "Apr", "May", "June", "July", "Aug", "Sept", "Oct", "Nov", "Dec"]
number = [1,2,3,4,5,6,7,
8,9,10,11,12]

# Using one input list
numdict = {x:x**2 for x in number}
print("Using one input list to create dict: ", numdict)

Conmpresion de listas vs map
### Comprensión de conjuntos 
set_a = {x for x in range(10,20) if x not in [12,14,16]}
print(set_a)
### Comprensión de generador
data = [2,3,5,7,11,13,17,19,23,29,31]
gen_obj = (x for x in data)
print(gen_obj)
print(type(gen_obj))
for items in gen_obj:
    print(items, end = " ")
  Son mas eficientes en memoria que las listas

## Excepciones
## Algoritmos
### Recursividad
Una funcion se llama a si misma
### divide y venceras
busqueda binaria
### programacion dinamica
Uso de modulos
### Codisioso
encuentra la mejor solución en todos y cada uno de los pasos en lugar de ser globalmente óptima
Manejo de Excepciones

try, except, finally
Creación de excepciones personalizadas
Algoritmos Comunes

Búsqueda binaria
Ordenamiento (QuickSort, MergeSort)
Búsqueda lineal
Algoritmos de grafos (Dijkstra, BFS, DFS)
Programación Dinámica

Problema de la mochila
Secuencia de Fibonacci
Subcadena común más larga
Recursividad

Definición y ejemplos
Casos base y casos recursivos
Comparación con iteración
Complejidad Algorítmica

Introducción a Big-O notation
Análisis de tiempo y espacio
Uso de Módulos y Bibliotecas

Introducción a módulos en Python
Bibliotecas populares (NumPy, Pandas, Matplotlib)
Estilos de Programación en Python

Programación orientada a objetos
Programación funcional
Programación imperativa
Pruebas Unitarias

Importancia de las pruebas
Uso de unittest y pytest
Documentación y Comentarios
Estilo de documentación (docstrings)
Mejores prácticas para comentarios

## Programación funcional
### Funciones puras (pure functions)
Es una funcion que no cambiara ningun valor a nivel global. Unicamente retornara cambios en las variables a las cuales le apliquemos la funcion.
```
def extend_function(lst, item):
  return lst + [item]

-> ejemplo 1
def retornar_cuadrado(item):
    return item**2

def suma_cuadrados(lst):
    return sum(list(map(retornar_cuadrado, lst)))

-> ejemplo 2
def suma_cuadrados(lst):
// usando list compreshion
  return sum([item** 2 for item ])

-> ejemplo 2
def retornar_cubo(n):
    return n**3

def sumar_cubos_pares(lst):
    return sum(map(retornar_cubo, [item for item in lst if item % 2 == 0]))

-> ejemplo 3
def multiplicar_y_filtrar(lst, n):
    return [item * 2 for item in lst if item > n]
-> ejemplo 4
def promedio_pares(lst):
    lst_pares = [item for item in lst if item % 2 == 0]
    return sum(lst_pares) / len(lst_pares) if len(lst_pares) > 0 else 0
-> ejemplo 5
def transformar_numeros(lst):
    return [item**3 if item % 2 == 0 else item**2 for item in lst]

```

### Funcion map:
En una estructura de datos iterable(como las listas), aplicara un metodo que especifiquemos, ejemplo, si queremos reversar strings de una lista, la usariamos así

```
list_coffes = ['capucchino', 'latte', 'with milk']
def reverseString(str):
  return str[::-1]
list_reverse = list(map(reverString, list_coffes))
```
## Recursividad
Una funcion se llama a si mismo, el objetivo es dividir una tarea en subtareas menos complejas.
### Reverse string with recursion

Paradigma de programación orientada a objetos (OOP)
Conceptos clave de OOP:
Clases
Objetos
Métodos
Cuatro conceptos fundamentales de OOP:
Herencia
Polimorfismo
Encapsulación
Abstracción

## map y filtrar
### map
Ejecuta una funcion a todos los elementos de un iterable, sin importar las conficiones internas
### filter
aplica una función a todos los elementos y solo retornara los elementos que cumplan una condicion de la funcion.
```

```
https://www.knowledgehut.com/blog/programming/python-map-list-comprehension
https://realpython.com/python-recursion/
https://stackabuse.com/functional-programming-in-python/


Paradigma de programación orientada a objetos (OOP)
Conceptos clave de OOP:
Clases
Objetos
Métodos
Cuatro conceptos fundamentales de OOP:
Herencia
Polimorfismo
Encapsulación
Abstracción

modificadores de acceso representados por palabras clave como public, private y protected.

class Alpha:

def __init__(self):
    self._a = 2.  # Protected member ‘a’
    self.__b = 2.  # Private member ‘b’

 Debe tenerse en cuenta que todavía se puede acceder a estos miembros privados y protegidos desde fuera de la clase utilizando métodos públicos para acceder a ellos o mediante una práctica conocida como name mangling. El name mangling es el uso de dos guiones bajos iniciales y un guión bajo final, por ejemplo:

_class__identifier 

Clase es el nombre de la clase e identificador es el miembro de datos al que quiero acceder.

# Herencia
class Parent:
    Members of the parent class

class Child(Parent):
    Inherited members from parent class
    Additional members of the child class

A medida que la estructura de la herencia se complica, Python se adhiere a algo llamado Orden de Resolución de Métodos (MRO) que determina el flujo de ejecución. MRO es un conjunto de reglas, o un algoritmo, que Python utiliza para implementar la monotonicidad, que se refiere al orden o secuencia en la que el intérprete buscará las variables y funciones a implementar. Esto también ayuda a determinar el ámbito de los diferentes miembros de la clase dada.

# Abstracción 
Abstracción
La abstracción puede verse tanto como un medio para ocultar información importante como información innecesaria en un bloque de código. El núcleo de la abstracción en Python es la implementación de algo llamado clases y métodos abstractos, que pueden implementarse heredando de algo llamado módulo abc. "abc" aquí significa clase base abstracta. Primero se importa y luego se utiliza como clase padre para alguna clase que se convierte en clase abstracta. Su implementación más sencilla puede hacerse como se indica a continuación.

from abc import ABC,   
class ClassName(ABC):
    pass

Creación de clases en Python

Se comienza creando un archivo y una clase, donde se definen variables y métodos que se pueden reutilizar en diferentes instancias.
Se utilizan dos métodos especiales: __new__ para crear un nuevo objeto vacío y __init__ para inicializar el objeto con valores específicos.
Instanciación y uso de métodos

# Herencia
# Clase padre
class Employees:
    def __init__(self, name, last):
        self.name = name
        self.last = last

# Clase hija que extiende la clase Employees
class Supervisors(Employees):
    def __init__(self, name, last, password):
        super().__init__(name, last)  # Llama al constructor de la clase padre
        self.password = password

# Otra clase hija que extiende la clase Employees
class Chefs(Employees):
    def leave_request(self, days):
        return f"May I take a leave for {days} days?"

# Creando instancias de las clases
adrian = Supervisors("Adrian", "A", "apple")
emily = Chefs("Emily", "E")
juno = Chefs("Juno", "J")

# Usando los métodos y variables
print(emily.leave_request(3))  # Solicita 3 días de permiso
print(adrian.password)           # Imprime la contraseña de Adrian
print(emily.name)               # Imprime el nombre de Emily

# Herencia multiple
# Example 1
class A:
   a = 1
   
class B:
   b = 2
   
class C(A, B):
   pass

c = C()
print(c.a, c.b)

# Prioridad de herencia
class A:
   a = 1

class B(A):
   a = 2

class C(B):
   pass

c = C()
print(c.a)
>> 2

# metodos utiles
issubclass(class A, class B)
Class A:
	pass
Class B(A):
	pass

b = B()
print(isinstance(b,B))
print(isinstance(b,B))

# ejemplo __super__
class Fruit():
    def __init__(self, fruit):
        print('Fruit type: ', fruit)


class FruitFlavour(Fruit):
    def __init__(self):
        super().__init__('Apple')
        print('Apple is sweet')

apple = FruitFlavour()




>>
>>Fruit type:  Apple
>>Apple is sweet

# clases abstractas

from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def hacer_sonido(self):
        pass

class Perro(Animal):
    def hacer_sonido(self):
        return "Guau"

class Gato(Animal):
    def hacer_sonido(self):
        return "Miau"
