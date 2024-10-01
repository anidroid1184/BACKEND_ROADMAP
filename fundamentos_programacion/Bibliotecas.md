# Bibliotecas
Cuando incluimos una librería en nuestra pagina web, aplicación web o sitio web, estás pueden llamarse "dependencias", dado a que nuestro código depende de estas para funcionar correctamente.
Las bibliotecas son código y funciones que podemos reutilizar que vienen de todo el internet, estas nos permite incluir diversas funcionalidades a nuestro código, para no tener que desarrollarlas desde 0.
Hay algunas funciones que son complejas de implementar, por lo mismo, las dependencias nos ahorran gran parte del tiempo de nuestro desarrollo.

Una librería conocida para el desarrollo CSS es "Boostrap" la cual nos permite agregar diferentes funcionalidades a nuestro sitio web, como notificaciones emergentes, listas desplegables, etc...
Tambien ofrece una librería para JavaScript que permite agregar muchas más funciones a nuestro sitio web.

Ahora, contémplatenos que un proyecto de desarrollo web puede tener multiples dependencias, que dependen unas de otras, en un solo archivo HTML, esto puede generar que el servidor demore en cargar mucho más tiempo el documento html y todas sus dependencias, para solucionar esto existen los "bundlers", estos permiten combinar en un solo archivo varios archivos pequeños. Por lo mismo permite combinar todas las dependencias en un solo archivo, a este proceso, que es automático, se le llama "bundling". Existen varias herramientas como "Gulp" y "WebPack" que nos permiten configurar cómo queremos que se realice el "bulding".
