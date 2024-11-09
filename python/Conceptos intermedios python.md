## List comprehension

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
