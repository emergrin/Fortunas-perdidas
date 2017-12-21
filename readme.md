# Como usar esto como una base para tus partidas

Escribo estas líneas para explicar someramente como editar estos archivos para adaptarlo a futuras partidas. Estos archivos han sido preparados para una partida llamada "Espejíto Espejíto" de Leyenda de los cinco anillos 4ª edición.

Esto no es mas que la transcripción de lo acontecido en la partida presentada, con mis cambios, apreciaciones y personal tratamiento.

Siente libre de tratarlo como una ayuda personal para el master, director de juego o como lo quieras llamar,  y como tal el  master siempre tiene la ultima palabra para adaptarlo a sus personajes.

Tecnológicamente todo está hecho con HTML, JavaScript y CSS. Yo no soy un experto en ninguna de las tres por eso la he recopilado de stackoverflow y otros foros similares.

Todo lo que aquí se contiene está bajo la licencia **CC BY-NC-SA de Creativ Commons**, esto es:*Esta licencia permite a otros entremezclar, ajustar y construir a partir de esta obra con fines no comerciales, siempre y cuando se reconozcan la autoría y sus nuevas creaciones estén bajo una licencia con los mismos términos.*

## Lo primero es crear un diagrama para cada escena

En el raíz de los ficheros tienes un archivo [.xml](./Espejito-espejito.xml) con los diagramas de cada escena, es un diagrama de flujo para adaptarse a los giros y cambios que la partida presente. Yo he usado una tool gratuita y online que está en [Draw.io](https://www.draw.io/).

Exporta cada diagrama como un PNG y almacenalo para usarlo en las futuras hojas como imagen de fondo.

## Lo segundo es crear una hoja html para cada escena

Cada escena debe tener una entrada con una hoja html donde existen varios elementos importantes:

1. **La matriz de coordenadas en la variable puntos**
```
{ x: 1, y: 1, z: 2, f: 2, id: "XXXXXX.html"},
```
Este mapa hace referencia al cuadrado formados por un punto (coordenadas x,y, la esquina superior izquierda) y su diagonal (coordenadas z,f, la esquina inferior derecha) y al nombre de la hoja html que tiene asociado como link (variable id).

Yo he usado GIMP para medir los puntos de cada elemento del diagrama y así añadirlo a este mapa.

**NOTA:** recuerda que cada línea debe terminar en una "," menos la última entrada que no la lleva.

2. **Directorio donde se buscaran las hojas html para cada punto**
```
var href = "e1/";
```
"e1" es el directorio donde irá a buscar el contenido de la variable "id" para cada punto.

3. **Asigna la imagen de fondo con el diagrama apropiado**
```
<img src="partida.png" usemap="#uno"><br/>
```
Usa la imagen de cada escena que has creado y ponla de fondo para la pagina designada

## Lo tercero crear la información necesaria para cada punto de los mapas con una hoja html

Todo lo que tienes que hacer ahora es crear dentro del directorio apropiado una hoja html simple (editando el texto dentro del body con el formato html). Te recomiendo que uses la que ya existe en las escenas de esta partida.

Recuerda que hay algunas hojas que contienen una tabla para poder ver al mismo tiempo una imagen, ficha o similar y el texto que quieras añadir.

## Por último solo tienes que editar la hoja menu.html

Edita la hoja [menu.html](./menu.html) para que corresponda con tus escenas creadas y/o añadir mas material que necesites (mapas, ayudas, etc).

## Recuerda disfruta de la partida con tus amigos
