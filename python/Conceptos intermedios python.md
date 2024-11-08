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
### Funcion map:
En una estructura de datos iterable(como las listas), aplicara un metodo que especifiquemos, ejemplo, si queremos reversar strings de una lista, la usariamos así

```
list_coffes = ['capucchino', 'latte', 'with milk']
def reverseString(str):
  return str[::-1]

list_reverse = list(map(reverString, list_coffes))

```
