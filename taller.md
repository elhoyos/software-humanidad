# La página de Sandra

## Repaso

Adaptación, retroalimentación

HTML

CSS

JavaScript


## Parte 1: contenido (HTML)

1. La página de Sandra la vamos a crear usando JSFiddle. Ingresa a https://jsfiddle.net.


2. Un documento HTML que pueda ser leído por un navegador web debe tener el siguiente código:

```html
<!DOCTYPE html>
<html>
  <body>
    Aquí va el contenido
  </body>
</html>
```

Aunque este código es muy importante, JSFiddle lo incluye por defecto por nosotros para nuestra comodidad y solo tendremos que escribir el contenido de la página de Sandra.

3. En un documento HTML el contenido debe ir dentro de etiquetas que abren `<h1>` y cierran `</h1>`. Por ejemplo, en `<h1>Encabezado</h1>` el texto dentro indica que es un encabezado. Incluye el siguiente encabezado al principio del recuadro "HTML" en JSFiddle:

```html
<h1>Sandra</h1>
<p>Por [tu nombre]</p>
```

4. `<p>Un párrafo</p>` se usa para indicar que el texto es un párrafo. Añade el siguiente texto introductorio:

```html
<p>Omnis dolorem ex temporibus est eum tempora. Est vero corporis dolorem. Ex vero consequatur in nemo voluptas numquam architecto. Ut laborum qui reiciendis pariatur perferendis.</p>
```

5. Para darle más estructura a la página, HTML nos permite distinguir entre el contenido introductorio y principal de un documento con las etiquetas `<header>` y `<main>`. 


```html
<header>
  <h1>Sandra</h1>
  <p>Por [tu nombre]</p>
  <p>Omnis dolorem ex temporibus est eum tempora. Est vero corporis dolorem. Ex vero consequatur in nemo voluptas numquam architecto. Ut laborum qui reiciendis pariatur perferendis.</p>
</header>
```

6. Cualquier etiqueta de HTML puede tener un identificador único en todo el documento (no se puede repetir). Este identificador se define con el atributo `id`.

```html
<main>
  <section id="historia"></section>
  <section id="fotos"></section>
  <section id="medios"></section>
</main>
```

7. Añade la historia de Sandra a la seccion correspondiente usando etiquetas `<p>`:

```html
<main>
  <section id="historia">
    <h2>Historia</h2>
  
    <p>
      Recusandae et quas deleniti nisi. Illum tenetur aut error. Voluptatibus reiciendis aut a qui vitae sunt quos. Id et voluptatem non sed. Occaecati aliquid et iusto earum.
    </p>

    <p>
      Omnis dolorem ex temporibus est eum tempora. Est vero corporis dolorem. Ex vero consequatur in nemo voluptas numquam architecto. Ut laborum qui reiciendis pariatur perferendis. Reprehenderit itaque commodi sed. Voluptas dolorem eos molestias assumenda accusamus omnis.
    </p>

    <p>
      Odit earum nobis vel quasi quisquam unde saepe. Accusamus blanditiis dolor qui laboriosam optio id nam. Ab qui eveniet adipisci assumenda. Accusamus consequatur in molestiae velit. In eligendi praesentium corrupti delectus ut accusantium dolores sapiente.
    </p>

    <p>
      Saepe repellendus impedit facere ut unde non minima molestiae. Nam reprehenderit vel natus eveniet voluptatem libero. Accusantium aut magnam tempora.
    </p>

    <p>
      Animi necessitatibus quis ea omnis iusto eaque doloribus. Et eaque autem sed eum et neque aliquam. Eveniet voluptate iste voluptatem occaecati est eum ratione. Error velit quam et qui. Quos officia quis ex ut. Id et ut maxime autem nesciunt facere consequatur repellat.
    </p>
  </section>
</main>
```

8. Con la combinación de etiquetas `<ul>` y `<li>` podemos crear listados no ordenados. Crea un listado con varios textos:

```html
  <section id="fotos">
    <h2>Fotos</h2>
    <ul>
      <li>
        Foto 1
      </li>
      <li>
        Foto 2
      </li>
    </ul>
  </section>
```

9. `<img>` nos permite incluir imagenes en nuestro documento. Para ello se debe indicar en el atributo "src" un localizador de la imagen. En nuestro caso, vamos a usar direcciones http como localizadores:

```html
  <section id="fotos">
    <h2>Fotos</h2>
    <img src="https://fotos.perfil.com/2019/11/07/trim/1140/641/sandra-the-orangutan-florida-802285.jpg" />
    <img src="https://ewscripps.brightspotcdn.com/dims4/default/3fb2115/2147483647/strip/true/crop/1000x563+0+0/resize/1280x720!/quality/90/?url=https%3A%2F%2Fewscripps.brightspotcdn.com%2Fcd%2Fd5%2F4fadad3b4e61a3ed00af99eaa7de%2Fwptv-sandra-orangutan.jpg" />
  </section>
```

10. Finalicemos el contenido del documento con una sección de medios de comunicación donde Sandra aparece. En esta sección utilizamos algunos de las etiquetas anteriormente aprendidas:

```html
  <section id="medios">
    <h2>Medios</h2>
    <p>
      He aparecido en diversos medios de comunicación. A continuación algunos de los cubrimientos de mi historia.
    </p>

    <ul>
      <li>
        <a href="https://www.npr.org/2020/09/21/915372713/sandra-sue-a-bosques">Sandra sueña bosques</a>, Radio Ambulante. Septiembre, 2020.
      </li>
    </ul>
  </section>
</main>
```

## Parte 2: estilo (CSS)

Luego de tener el contenido de la página en JSFiddle, vamos a darle un toque de estilo CSS.

1. Con CSS podemos cambiar el estilo de las etiquetas del documento HTML. Como se muestra en el ejemplo a continuación, podemos ajustar el color del texto de todo el cuerpo del documento:

```css
body {
  color: #566b78;
}
```

2. Las lineas de texto largas son difíciles de leer. Limitar el número de caracteres entre 45 y 85 mejorará la capacidad de la página para ser leída. Para ello, vamos a organizar el diseño del documento en tres columnas, la del centro representa el contenido.

Añade la *clase* "contenedor" a `<header>` y `<main>`:

```html
<header class="contenedor">
...
</header>

<main class="contenedor">
...
<main>
```

3. Ahora, divide el contenido de cada elemento "contenedor" en una cuadrícula (*grid*) de tres columnas. Cada valor del estilo `grid-template-columns` es una columna como se muestra a continuación:

```css
/*
  El texto entre un "/*" y su inverso, es un comentario
  que no tiene ningún efecto.
*/

.contenedor {
  display: grid;
  grid-template-columns: 
    1fr               /* Columna 1 */
    min(65ch, 100%)   /* Columna 2 */
    1fr;              /* Columna 3 */
}
```

**TODO:** Explicar las unidades fr, ch y % 

4. Asigna a todos los elementos internos de cada "contenedor" a la columna del centro (i.e. la Columna 2):

```css
.contenedor > * {
  grid-column: 2;
}
```

5. Por defecto, nuestros navegadores usan la fuente "Times". Para hacer la página más agradable, cambiemos el texto a una fuente "sans-serif" (sin ...) como "Helvetica" o "Arial".

**TODO:** Explicar por qué ponemos todas las familias mencionadas?

```css
body {
  font-family: "Helvetica", "Arial", "sans-serif";
}
```

6. Añadir espacio *antes* y *después* de las lineas de texto hará que la página se vea más atractiva:

```css
body {
  line-height: 1.5;
  padding: 4em 0em;
}

h2 {
  margin-top: 1em;
  padding-top: 1em;
}
```

7. Aumenta el contraste del texto para una mejor lecturabilidad:

```css
h1,
h2,
strong {
  color: #333;
}
```

8. Acentúa visualmente los elementos interactivos de la página, como los vínculos de la sección "Medios":

```css
a {
  color: #e81c4f;
}
```

9. Mejora la apariencia inicial del encabezado de la página con una imagen de fondo de [Unsplash](https://unsplash.com/photos/lDy1K7RkLeA). Le vamos a indicar al navegador que:

* En caso que la imagen no se cargue, utilice un color oscuro como #263d36. Esto para ayudar a contrastar con un texto de color blanco (*white*).
* Posicione la imagen en su centro y en su parte de abajo, para que se muestre la parte más oscura de la imagen e igualmente mejorar el contraste con el texto blanco.
* No repita la imagen de fondo en caso que la pantalla sea muy grande.
* Con `background-size: cover` indicamos al navegador que escale la imagen tanto como pueda de acuerdo a su contenedor sin alargarla y reducirla.

```css
header {
  background-color: #263d36;
  background-image: url('https://images.unsplash.com/photo-1583470790878-4f4f3811a01f?ixlib=rb-1.2.1&auto=format&fit=crop&w=1955&q=80');
  background-position: center bottom;
  background-repeat: no-repeat;
  background-size: cover;
  text-align: center;
}

header > * {
  color: white;
}
```

10. Organiza el listado de fotos de Sandra.

```html
<section id="fotos">
  <h2>Fotos</h2>
  <div class="galeria">
    <img src="https://fotos.perfil.com/2019/11/07/trim/1140/641/sandra-the-orangutan-florida-802285.jpg" />
    <img src="https://ewscripps.brightspotcdn.com/dims4/default/3fb2115/2147483647/strip/true/crop/1000x563+0+0/resize/1280x720!/quality/90/?url=https%3A%2F%2Fewscripps.brightspotcdn.com%2Fcd%2Fd5%2F4fadad3b4e61a3ed00af99eaa7de%2Fwptv-sandra-orangutan.jpg" />
    <img src="https://s26643.pcdn.co/wp-content/uploads/2020/06/chimp-traveling-over-creek-1030x773.jpg" />
  </div>
</section>
```

**TODO:** explain grid-column

```css
.galeria {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(12em, 1fr));
  grid-gap: 20px;
  align-items: center;
}

.galeria > img {
  border: 1px solid #ccc;
  box-shadow: 2px 2px 6px 0px rgba(0,0,0,0.3);
  max-width: 100%;
}
```