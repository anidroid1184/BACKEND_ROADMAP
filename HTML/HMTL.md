# HMTL
HTML es un estándar en el mundo de la programación web, ya que brinda la estructura de básica de las paginas web que conocemos, sus siglas traducen: Lenguaje de Marcado de Hipertexto. Este lenguaje se centra en marcar y delimitar con etiquetas las diferentes secciones de una pagina web, teniendo etiquetas de texto, encabezados, imágenes, enlaces, párrafos, tablas, saltos de líneas, etc...
Aunque hay diferentes frameworks que permiten el desarrollo de paginas web a través de métodos, HTML sigue siendo la base para todo el desarrollo web conocido.

A continuación veremos la estructura básica de un documento html:
```
<!DOCTYPE html> --> Esta etiqueta le dice al navegador el formato del documento
<html> --> Etiqueta de mayor nivel que contendrá el resto de etiquetas en ella
<head> --> En esta sección van apartados como las hojas de estilo, algunos datos de la pagina, el lenguaje y el titulo de la pestaña
	<title>Title of the document</title> --> Titulo de la pestaña
</head> --> Cierre de la etiqueta


<body> --> Cuerpo principal del documento
Acá se vera todo el contenido visible de la pagina

Etiquetas para diferentes tamaño de titulo en orden de mayor a menor tamaño:
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>
  <h3>Heading 3</h3>
  <h4>Heading 4</h4>
  <h5>Heading 5</h5>
  <h6>Heading 6</h6>
 Parrafos: 
Los párrafos permiten escribir diversos textos en forma de bloque en el documento, también hay etiquetas para resaltar texto
Cuando usamos 
<p>
Esto es un párrafo <br> --> Salto de linea

<strong>Esto sera una linea será importante </strong> --> strong denota que lo que se encuentre dentro será importante

<b> Atracción </b> --> Negrita se usa cuando queremos llamar la atención del lector

<em> Énfasis </em> --> La usamos para hacer énfasis en una area del texto

<i> Inclinado </i> --> Lo usamos para mostrar texto inclinado


</p>

Listas

Estas etiquetas se usa al momento de hacer una lista:

Lista NO-ordenada
<ul>
	<li>Elemento1</li>
	<li>Elemento2</li>
	<li>Elemento3</li>
</ul>

Lista ordenada
<ol>
	<li>Elemento1</li>
	<li>Elemento2</li>
	<li>Elemento3</li>
</ol>


DIV: define una división de contenido en el documento HTML
Pueden ser útiles para aplicarles estilos a secciones especificas de nuestra pagina.
<div>
	<p>
		Este párrafo está dentro de una división div
	</p>
</div>

<a href="document.html">Enlace a otra pagina web></a> --> Esta etiqueta nos permite enlazar nuestras paginas web y otras cosas.

<img src="ruta.png" alt"Nombre_auxiliar"> --> Esta etiqueta sirve para indicar donde vamos a insertar una imagen, también 					      tiene parámetros como width y height para modificar su tamaño.


TABLAS:

<table>
	<tr> -->Indicar una nueva columna
		<th>Encabezado de tabla1</th> -->Etiqueta para indicar el texto de el encabezado 
		<th>Encabezado de tabla2</th>
	</tr>
	
	<tr>
		<td>Soy un dato de la tabla1</td> -->Etiqueta para indicar el contenido de las tablas
		<td>Soy un dato de la tabla2</td>

	</tr>
</table>

Esta etiqueta es muy util para mostrar información como tablas de precios o menus de forma clara, no obstante, si no agregamos estilos no podrá verse claramente

Con este fragmento podemos estilizar la tabla muy fácilmente:
<style> 
	table, th, tr {
		border: 1px solid black;
		border-collapse: collapse;
	}
</style>
</body>--> Cierre de la etiqueta

</html> --> Cierre de la etiqueta

<!-- Esto es un comentario -->

``` 
Secciones las cuales el código ignora y nos pueden servirnos para darle un orden.


