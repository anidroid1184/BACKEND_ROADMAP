# Tour por GO

Go o Golang es un gran lenguaje que se ha convertido en uno de los más prometedores a futuro, debido a su facilidad de sintaxis y su capacidad de manejar memoria como se hace con C.
Ahora, ¿cuales son las partes básicas de este? Vamos a verlas:

## Paquetes 
Cada programa en go se compone por paquetes, el paquete "main" es el básico de cualquier programa para su correcto funcionamiento. También podemos importar diferentes paquetes para agregar funciones soportadas a nuestro código. 
En las importaciones por convención, se importan los métodos específicos que queremos usar únicamente de la importación, aunque también podemos importar la librería completa.
Ahora veremos un ejemplo de código básico en el cual hacemos la importación del modulo "math/rand", el cual usamos para generar una numero entero aleatorio:

```
package main --> importamos el paquete main

import (
	"fmt"-->Librería completa
	"math/rand"--> De la librería math. extraemos la sublibreria rand
)

func main(){
	fmt.Println("Mi número favorito es", rand.Intn(10))
	fmt.Println("El número favorito de mi novia es", rand.Intn(10))
}
```

## Importaciones
La comunidad de go es muy activa, brinda gran cantidad de contribuciones constantes a las funciones que podemos tener con este lenguaje, ademas, qué necesitamos de ciertas librerías por defecto para poder correr un codigo común, por lo mismo, es normal ver librerias como "fmt".
Podemos realizar varias importaciones en una sola instrucción de importación factorizada, si hacemos varias importaciones es buena practica relizarlo así:
```
package main

-->Importaciones:
 import (
	"fmt"
	"math"
)

func main(){
	fmt.Printf("Hola, la raíz cuadrada de 2 es :\n", math.Sqrt(2))+
}


--Nombres exportados

Podemos decir que son similares a los métodos de python, que vienen una importación de paquetes, estos nombres exportados vamos  siempre a escribirlos con mayuscula inicial, de lo contrario nos generara errores:

package main

import (
	"fmt"
	"math"
)

func main() {
	fmt.Println(math.Pi)--> Nombre exportado Pi
}
```
## Funciones

Las funciones son fragmentos de código reutilizables, los cuales son extremadamente útiles en programación, dado a que nos permite hacer nuestro código mucho más corto y menos repetitivo, por ende, más eficiente.

Ahora, para declararlas en go deben están en el nivel de package main e import:

```
package main

import "fmt"

func add(x int, y int) int {
	return x+y
}
```
Como podemos notar, la sintaxis de la función es la sgte:

- El nombre de la función va después de la declaración de esta.
- Dentro de paréntesis debemos especificar los tipos de las variables internas de la función.
- Después de definimos el tipo del retorno de la función.
- Escribimos entre corchetes que hará la función.

Ahora, también podemos "factorizar" la declaración de tipos de variable, solo indicando el tipo en la última variable que la tenga.

```
package main 

import "fmt"

--> Factorizamos el tipo de variables

func add(x, y, z int) int {
	return x+y+z
}

func main() {
	fmt.Printl(add(42, 13))
}
```
Tambien podemos retornar más de una variables, por lo mismo, debemos especificar también el tipo de las salidas:

```
package main

import "fmt"

func swap(x,y string) (string, string) {
	return y,x
}


func main() {
	a,b := swap("Hola", "mundo")
	fmt.Println(a,b)
}
```

También, para variables internas la cuales pueden ser nombradas en la parte superior de la función, además, una función que no retorne nada, retornara estas variables internas, esto se conoce como retorno desnudo ("naked" return).

```
package main

import "fmt"

func split(sum int) (x, y int) {
	x = sum * 4/9
	y = sum - x
	return 
}


func main() {
	fmt.Println(split(17))
}

>> 7 10
```

## Variables

Podemos definir n variables en una lista de variables con la sentencia "var", donde también podemos hacerlo en la función main y al nivel de "package main":

```
package main

import "fmt"

var c, python, java bool  --> podemos declarar varias variables al mismo tiempo

func main() {
	var i int --> También 
	fmt.Println(i, c, python, java)
}
```
También podemos declarar un valor de inicio junto con las variables, de la misma forma, en la lista de variables.
```
package main

import "fmt"

var i, j int = 1, 2

func main() {

	var c, pyhton, java = true, false, "no!"
	fmt.Println(i, j, c, python, java)
}

>> 1, 2, true, false, "no!"
```

## Declaración corta de variables

La declaración var necesita asignar un tipo de dato implicito cada que la usamos, dentro de la función main, podemos declarar variables de forma más corta usando el operador ":=".

```
package main

import "fmt"

func main() {
	var i, j int = 1, 2
	k := 3
	c, python, java := true, false, "no!"
	
	fmt.Println(i, j, k, c, python, java)
}
>> 1, 2, 3, true, false, "no!"
```
Fuera de la función main, toda declaración debe empezar con una palabra clave.

### Tipos básicos de variables en GO:

#### bool --> Booleano

#### string --> Cadena

#### int --> entero normal, suele tener 32 bits de longitud en sistemas de 32 y 64 bits.

###### Cuando contienen un número, este representa la longitud de la variable siendo el máximo int64... int8, int16, int32, int64

##### uint --> int unsigned de 32 bits de longitud, tenemos longitudes de uint8, uint16, uint32, uint64,  Se usa cuando el número no es negativo, es decir, el valor nunca será negativo.

##### uintptr --> unsigned integer enough to store the uninterpreted bits of a pointer value, tenemos longitudes como uintptr8, uintptr16, uintptr32, uintptr64, es un entero que no tiene signo y que tiene el mismo tamaño que un puntero.

##### byte --> alias para uint8

#### rune --> alias para int32 y representa un punto de código Unicode, representa un número asociado a un carácter especifico en el estándar Unicode.

#### float32, float64 --> Numero flotantes de 32 y 64 bits

#### complex64, complex128 --> Números flotantes de 64 y128 bits.


En el sgte ejemplo vemos un caso de uso de declaraciones factorizadas

```
package main

import (
	"fmt"
	"math/cmplx"
)

var (
	ToBe	bool	=false
	MaxInt	uint64	=1<<64 -1
	z	complex128 = cmplx.Sqrt(-5 + 12i)
)

func main() {
	fmt.Printf("Tipo: %T Valor: %v\n", ToBe, ToBe)
	fmt.Printf("Tipo: %T Valor: %v\n", MaxInt, MaxInt)
	fmt.Printf("Tipo: %T Valor: %v\n", z,z)
}

>Tipo: bool Valor: false
>>Tipo: uint64 Valor: 18446744073709551615
>>Tipo: complex128 Valor: (2+3i)
```

Como podemos observar en el bloque anterior, al mostrar un texto podemos usar diferentes formar para mostrar las variables para imprimir en pantalla.
```
%T --> tipo de la variable
%v --> valor de la variable
\n --> Salto de lineal
```

## Valores por defecto 

### 0 tipos numéricos
### false para tipo bool
### "" para strings


Podemos ver un ejemplo donde vemos estos valores predeterminados:

```
package main
import "fmt"

func main() {
	var i int
	var f float64
	var b bool
	var s string
	fmt.Printf("%v %v %v %v  %q\n", i, f, b, s)
}
>> 0 0 false ""
```

## Conversión de tipos

Podemos convertir variables a otros tipos declarando de la forma "Tipo(variable_trasnformar)":

Algunas conversiones con var:

```
var i int = 42
var f float64 = float64(i)
var u uint = uint(f)
```

También podemos convertir a otro tipo usando la definición corta
```
i:= 42
f := float64(i)
u := uint(f)
```
Con var también lo podemos hacer de la sgte forma:
```
var f = math.Sqrt(float64(x*x + y*y))
var z = uint(f)
```
Por lo mismo no es necesario usar toda la sentencia donde repetimos el tipo de dato dos veces.

inferencia de tipo

Si declaramos una variable a partir de otra, esta nueva variable tomara el tipo de la variable de referencia.

Ejemplo: 
```
var i int
j:= i// j es int como lo es i
```


Si asignamos una constante, esta tomara el tipo dependiendo al aproximación más cercana al tipo asignado:
```
i := 42		//int
f := 3.142	//float64
g := 0.532 +0.5i//complex128
```
## Constantes

Son variables que no cambiaran su valor declarado en todo el programa, se declaran con la palabra clave "const".

Estas constantes puede ser caracteres, cadenas de texto, booleanos o valores numéricos.

Las constantes no se pueden declarar usando la sintaxis ":=".

Ejemplo de uso:
```
package main

import "fmt"

const Pi = 3.14

func main() {
	const World = "Mundo"
	fmt.Println("Hola", World)
	fmt.Println("Feliz día de", Pi)
	
	const Truth = true
	fmt.Println("Go manda?", Truth)
}
```
## Constantes numéricas

Las constantes numéricas con valores de alta precisión, que toma el tipo que necesita según su contexto.

Recordemos que un int puede solo imprimir máximo un numero de menos de 64 bits de longitud, por lo mismo debemos evitar desbordar la capacidad de la variable.

```
package main

import "fmt"

const (
	// Crear un número enorme desplazando 1 bit a la izquierda 100 lugares.
	// Es decir, el número binario que es 1 seguido de 100 ceros.

	Big = 1 << 100 //creamos un número enorme desplazando 1 bit a la izquierda
	 
	// Por el contrario, podemos crear un número minúscula desplazando un bit a la 		// derecha
	
	Small = Big >> 99
)

func needInt (x int) int {
	return x *0.1
}
func needFloat(x flaot64) float64 {
	return x*0.1
}

func main () {
	fmt.Println(needInt(Small))
	fmt.Println(needFloat(Small))
	// fmt.Println(needInt(Big)) --> Esta variable se desbordara y no permitirá 	//imprimir
	fmt.Println(needFloat(Big))
}

>>21
>>0.2
>>1.2676506002282295e+29
	
```




Extraido de "Tour por Go"
