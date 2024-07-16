# aprende-css-basico-construyendo-un-menu-de-cafeteria

Página web creada en el curso "Aprende CSS básico construyendo un menú de
cafetería", perteneciente a la certificación "Diseño Web Responsivo" de
freeCodeCamp.

---

[Enlace a la web](https://cafe-menu-bde.netlify.app/)

---

# Aprende CSS básico construyendo un menú de cafetería

- Como ya aprendimos en el proyecto "Cat Photo App", hay una estructura básica para construir una pagina web. El elemento `<DOCTYPE html>` y el elemento `<html>` incluyendo el atributo `lang`  para especificar el idioma que usara el contenido de la pagina.

- El elemento `<style>` nos permite agregar estilo a cualquier componente de nuestra pagina web. Dentro de este elemento, podemos especificar el estilo para cada uno de los componentes de nuestra pagina.

- La sintaxis a utilizar para  estilar un elemento es:

  	```
	elemento {
		propiedad: valor;
	}
	```
   
- Si varios elementos comparten la misma funcionalidad de estilo, en lugar de escribir el mismo bloque de código para cada uno de los elementos, podemos hacer que todos los elementos compartan el mismo bloque de código. Para ello basta con escribir todos los componentes en una misma lista, separados por comas.

	Ejemplo:
	```
	h1, h2, p {
		propiedad: valor;
	}
	```
 
- En lugar de añadir estilo a nuestros elementos insertándolos dentro del elemento `<style>`, es recomendable crear un archivo externo y desde el documento .html acceder a este. Por conveniencia, el archivo externo se nombrara como "style.css". Es importante tener en cuenta que no pueden haber un elemento `<style>` y un archivo .css externo juntos en un mismo documento .html .

- Para indicarle al documento .html  cual es la hoja de estilos que debe de usar y donde esta se encuentra, utilizamos el elemento de auto-cierre `<link>` con la siguiente sintaxis:

  	```
	<link rel="stylesheet" href="styles.css">
   	```
   
	Como podemos ver, se utilizan los atributos `rel` (que indican al documento .html  que tipo de hoja es) y `href` (que indica la ruta de la hoja de 		estilos). En este caso los dos documentos (.html y .css ) se encuentran en el mismo directorio.

- Existe un elemento `<meta>` que ayuda a que nuestra pagina se vea bien tanto en ordenador de escritorio como en dispositivos móviles. Su nombre es **viewport**  y la sintaxis es la siguiente:

  	```
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
   	```

- La propiedad `background-color` especifica el color de fondo del elemento.

- El elemento `<div>` se utiliza principalmente para propósitos de diseño y es un elemento de _bloque_.
  
- El elemento `<span>` también es para propósitos de diseño. Al contario que `<div>`, `<span>` es un elementp _inline_

- La propiedad CSS `width` nos permite asignar un ancho especifico a cada elemento de nuestra página.

- También podemos establecer un ancho especifico mediante porcentajes. El elemento usará el tanto por ciento del ancho de su elemento padre.

- Podemos especificar el componente que será estilizado mediante su `id` . para señalar a un componente por su `id` anteponemos a su id  una almohadilla.
	Ejemplo:
		```
		#menu {}
  		```

- Los comentarios en CSS se envuelven entre `/*`  y  `*/`

- Para centrar un `<div>` horizontalmente debemos de dar el valor `auto`  a las propiedades `margin-left`  y  `margin-right` , dentro del elemento que queremos centrar.

- Los márgenes (`margin`) son espacios invisibles entre el elemento hijo y el elemento padre.

- Aunque lo selectores de tipo (p) y los selectores id (#) son validos, es más común utilizar los selectores de clase. un selector de clase se indica anteponiendo un punto al nombre de su clase:
  	```
	.menu{}
   	```

- Evidentemente, es necesario darle al elemento que queremos estilizar el atributo `class` .

- Con `backgroung-image` podemos hacer que el fondo de la página sea una imagen:
  	```
	background-image: url(https://…);
   	```

- Dos párrafos puede ser perfectamente una sección (`<section>`)

- El elemento parrafo es un elemento de bloque. Si queremos unir dos elementos `<p>` en una misma linea, podemos usar la propiedad-valor `display: inline-block` .

- Pero existe un problema si hacemos lo descrito arriba, los dos `<p>` no quedaran exactamente uno al lado del otro, habiendo un salto de linea entre ambos elementos. Esto es así porque el primer elemento toma el ancho total del elemento padre. Podríamos arreglas esto dándole un ancho del 50% a cada elemento, de ese modo se repartirían la mitad de la linea cada uno. Aunque, si hacemos la prueba esto no es del todo cierto. Esto crea un espacio extra a la derecha del primer elemento. Para arreglarlo existe un truco, darle a cada elemento un ancho del 49%. Voila! ya funciona como esperábamos.

- Lo descrito arriba funciona, aunque aun no del todo. El elemento a la derecha de la linea tiene muy poco espacio con el margen derecho del padre. Para solucionarlo, debemos de situar ambos elementos `<p>` en una misma linea uno junto a otro en el editor de texto, sin espacio entre ellos.  Además de esto volvemos a dar a los elementos `<p>` un ancho del 50%. Ahora si!, funciona 100%.

- Como tenemos el ancho de cada elemento `<p>` configurado al 50%, si reducimos el ancho de la ventana del navegador, llegará un punto en el que el nombre de los diferentes sabores de café utilicen dos lineas. Esto es así porque cada elemento `<p>` utiliza el 50% del espacio. Como sabemos que el elemento `<p>`  que muestra el precio tiene menos caracteres, podemos dar mas espacio al elemento `<p>` con el texto de los sabores, por ejemplo 75% sabor y 25% precio. De este modo habrá que reducir muchísimo el ancho del navegador para que el párrafo con el texto de sabor se separe utilizando dos lineas. Moraleja: ajusta el ancho de línea para cada elemento `<p>` con sentido común, dependiendo del tipo de contenido que vaya a mostrar.

- Propiedades `padding`  para crear espacio entre los elementos y su entorno.

- La propiedad `padding` sin argumentos específicos (top, right, bottom, left) aplicará el valor dado a los cuatro lados de la página. el orden de los argumentos debe de ser el mismo descrito entre paréntesis, es decir en sentido contrario al movimiento de las agujas del reloj.

- La propiedad `margin` sin argumentos específicos, funciona igual que la
  propiedad `padding` , es decir con los argumentos sin especificar escritos en el
mismo sentido (contrario al movimiento de las agujas del reloj).

- Con la propiedad `max-width` podemos ajustar el ancho máximo que tendrá el elemento con respecto a su componente padre.

- La propiedad `font-family`  nos permite asignar un determinado tipo de fuente (letra). Si no especificamos ningún tipo de fuente, por defecto el navegador asignara la que tenga predeterminada.

- Es una buena practica anadir una fuente de resplado que acompane a la ya dada en `font-family` . Con ello nos aseguramos de que exista una alternativa, si la fuente que hemos especificado no está disponible. Añade tantas fuentes de respaldo como consideres necesario, añadiendo cada fuente separada por una coma.

- La propiedad `font-style`  aplica estilos a la fuente. Estos estilos pueden ser normal, italic (cursiva) y oblique .

- `font-size` para establecer el tamaño de la fuente.

- El elemento `<hr>` inserta una linea divisoria que separa contenido.

- `<hr>`  por defecto presenta una linea delgada. Podemos modificar el ancho de la linea utilizando el atributo `height` , dándole un tamaño de pixeles mayor. 	Ademas, podemos cambiar el color de la linea con la propiedad `background-color` .

- La propiedad `background-color` cambiará el color de fondo, pero para cambiar el color del borde de la línea utilizaremos la propiedad `border-color` .

- Por defecto, el elemento `<hr>` tiene un grosor para los bordes de 1px.

- Los comentarios se insertan entre `/*` y `*/` 

- Usualmente, el color de un `<link>` que no ha sido clicado es azul y el `<link>` que si ha sido clicado es morado.

- Podemos cambiar el comportamiento de color por defecto de los `<link>` que aun no han sido clicados, añadiendo al elemento ´<a>` la propiedad `color` .

- Para cambiar el comportamiento de los `<link>` que si han sido clicados, utilizamos el pseudo-selector :
  	```
	a:visited { nombreDeLaPropiedad: valorDeLaPropiedad }
   	``` 

- Un **pseudo-selector** o **pseudo-clase** es una palabra clave de CSS que se anade a los selectores y que especifica un estado especial del elemento 		seleccionado (Mozilla Developer-Network).

- El pseudo-código `a:hover`  modifica el estado de un enlace (link) cuando el usuario coloca el puntero del ratón sobre el texto del enlace.

- El pseudo-código `a:active`  modifica las propiedades de un enlace cuando este está siendo presionado.

- Los elementos `<h1>` , `<h2>` , etc … , tienen un margen por defecto predeterminado por el navegador. Para modificar dichos margenes podemos utilizar la propiedad `margin`  en sus variantes `top` , `bottom` , `left`  y/o `right` .

- Las imágenes son elementos de tipo _inline_ . Si queremos que una imagen se comporte como un elemento de _bloque_, como por ejemplo un título (h1), podemos añadirle la propiedad `display`  con el valor `block` . De ese modo, podremos por ejemplo centrar la imagen horizontalmente con `margin-left: auto; margin-right: auto;` .

- Los valores de las propiedades tambien pueden ser **negativos**. Como ultimo ejercicio, para terminar la pagina web con el menu de cafeteria,damos a las imágenes (que son los iconos bajo los titulos h2) un valor de `margin-top: -25px;` . Con esto conseguimos que los iconos queden mas cerca de sus respectivos títulos.

- Fin
