# HTML

<div align="center">

![img](https://cdn-icons-png.flaticon.com/256/174/174854.png)

</div>

Html no es un lenguaje de programación, es un lenguaje de marcado por lo que no estará compuesto por sentencias de código si no por etiquetas y atributos mayormente.
Está creado mayormente para el diseño de páginas web.

## Conceptos básicos

Una etiqueta es un elemento que siempre abriremos y cerraremos usando *< > /* .

Ejemplo:

```html
 <etiqueta> 
 </etiqueta>

 <etiqueta2/>
 ```

 En este ejemplo tenemos dos formas de representarlo, la primera abrimos un elemento etiqueta(&lt;etiqueta&gt;) que luego cerramos (&lt;/etiqueta&gt;). Y otra forma que es cerrando la etiqueta en la misma línea (&lt;etiqueta/&gt;). Ambas formas, aunque ahora no sepamos para que usarlas, representan un elemento vacío.

Ejemplos de etiquetas:

```html
 Párrafo:
 <p>
    Esto es un párrafo
 </p>
 
 Encabezado:
 <h1>
    Encabezado tamaño grande
 </h1>
 ```

Los atributos por el contrario, van dentro de las etiquetas (puede haber uno o varios atributos en una etiqueta) proporcionando información adicional sobre estas. No todas las etiquetas
tendrán los mismos atributos ya que algunos son específicos de una etiqueta. Los atributos vendrán dados de forma *clave="valor"*.

```html
 <etiqueta clave="valor">
 </etiqueta>

 <etiqueta2 clave2="valor2"/>
```

También podremos encontrarnos con comentarios dentro de html, los comentarios son bloques de texto los cuales no afectarán al código y sirven para aportar información que no se mostrará en el navegador una vez hagamos una página.

```html
<!-- Esto es un comentario-->

<!-- Esto
     es
     un
     comentario
-->
```

## Estructura de una página web

Las páginas web siempre tendrán las siguientes etiquetas.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>
        </title>
    </head>
    <body>
    </body>
</html>
```

Esta es la estructura básica que todas las páginas web que veas tendrán, pueden tener más etiquetas, pero estas siempre las tendrán.

### Head

La etiqueta head no es para mostrar contenido dentro de la página, se usa para contener metadatos de la página.

Suele haber dentro una serie de etiquetas, que pueden o no estar.

&lt;title&gt;: Representa el texto que aparecerá en la pestaña del navegador.

&lt;meta&gt;: Se usa en conjunto de atributos para proporcionar metadatos sobre la página web. (&lt;meta charset="UTF-8"/&gt; Nos sirve para la codificación de caracteres de nuestra página.)

### Body

Esta etiqueta es en la que irá el contenido que se muestra en la página, todo lo que serían textos, imágenes, formularios y demás aspectos visuales.

Algunas de las etiquetas más usadas son:

#### Texto

- Encabezados

    &lt;hx&gt; : x es un numreo ue va desde el 1 hasta el 6 donde 1 es el encabezado más grande y 6 el más pequeño.

- Formato
  
    &lt;b&gt;...&lt;/b&gt; : Para resarltar en negrita.

    &lt;i&gt;...&lt;/i&gt; : Para poner las letras en cursivas.

    &lt;del&gt;...&lt;/del&gt; : Para que aparezca tachado con una línea.

    &lt;sub&gt;...&lt;/sub&gt; : Para poner cosas abajo-derecha del contenido como  un subindice.

    &lt;sup&gt;...&lt;/sup&gt; : Para poner cosas arriba-derecha del contenido como un superindice.

    &lt;mark&gt;...&lt;/mark&gt; : Para subrayar el texto.

    &lt;p&gt;...&lt;/p&gt; : Para agrupar en párrafos.

    &lt;/br&gt; : Para hacer un salto de línea.

    &lt;/hr&gt; : Para hacer una separación de tema con una línea.

#### Enlaces

- Imágenes

    &lt;/img ...&gt; : La etiqueta img suele utilizarse con atributos y no suele tener contenido.

  - Atributos:
  
    src: Ruta que ndica donde está la imagen a mostrar. La ruta puede ser relativa (dentro del proyecto html), absoluta (en un archivo de nuestro ordenador) o una url (imagen de internet).

    alt: Texto alternativo para la imagen.

    height: Altura de la imagen.

    width: Anchura de la imagen

- Figure

    Nos sirve para asociar un texto a una imagen, es decir, visualmente es algo que se podría hacer con img y un texto debajo, pero conceptualmente decimos que todo pertenece a un mismo elemento.

    ```html
    <figure>
        <img ....>
        <figcaption>Texto asociado</figcaption>
    </figure>
    ```

- Enlaces

  - Externos

    &lt;/a....&gt;...&lt;/a&gt; : Nos sirve para crear un hipervínculo. Dentro del contenido puede ir una imagen, tabla, etc  , lo que queramos que alguien pinche para llevarlo a otro sitio.

    Suele tener 2 atributos principales href y target.

    href: Para indicar la ruta del documento/página a donde ir.

    target: En que pestaña se abrirá (_blank para pestaña nueva, no poner para misma pestaña)

  - Internos

    Para enlazar elementos de dentro de tu mismo documento html haremos los siguiente:

    ```html
        <a href="#marca">....</a>
        ....
        ....
        ....
        <p id="marca">...</p>
    ```

    Con esto enlazaríamos lo que haya dentro de la etiqueta enlace (&lt;a&gt;), para que cuando pinchen en ello nos lleve al párrafo designado.

#### Listas

Hay tres tipos de listas ordenada, desordenada y de definición.

- Ordenada

    ```html
    <ol>
        <li>Primer elemento</li>
        <li>Segundo elemento</li>
        <li>Tercer elemento</li>
        .....
    </ol>
    ```

    Una lista ordenada, como su nombre indica, muestra los elementos en orden, es decir, numerados.

    El elemento  &lt;ol&gt; indica que es una lista ordenada y  &lt;li&gt; lo usamos para cada elemento de la lista. La numeración se hace automáticamente.

- Desordenada

    ```html
    <ul>
        <li>Primer elemento</li>
        <li>Segundo elemento</li>
        <li>Tercer elemento</li>
        .....
    </ul>
    ```

Al contrario que las ordenadas, las listas desordenadas no indican ningún orden simplemente nos ponen cada elemento con figuras delante ( circulos, circunferencias...).

- De definición

    ```html
    <dl>
        <dt>Primer elemento</dt>
        <dd>Descripción del primer elemento</dd>

        <dt>Segundo elemento</dt>
        <dd>Descripción del segundo elemento</dd>
        .....
    </dl>
    ```

Las listas de definición las usaremos en contextos donde queramos ir definiendo cada elemento de la lista.

#### Tablas

- `<table> ... </table>` : Etiqueta principal que encierra toda la tabla.

- Filas

  `<tr> ... </tr>` : Table Row → Define una fila dentro de la tabla.  
  Dentro de ella van las celdas.

- Celdas

  - `<td> ... </td>` : Table Data → Define una celda de **contenido normal**.  
  - `<th> ... </th>` : Table Header → Define una celda de **cabecera** (por defecto el texto aparece en negrita y centrado).

- Agrupación de partes

  - `<thead> ... </thead>` : Agrupa la cabecera de la tabla.  
  - `<tbody> ... </tbody>` : Agrupa el cuerpo de la tabla (las filas de datos).  
  - `<tfoot> ... </tfoot>` : Agrupa el pie de la tabla (por ejemplo, totales).

- Atributos útiles

  - `border` : Añade borde a la tabla y celdas (ej: `<table border="1">`).  
  - `colspan` : Une varias columnas en una celda.  
  - `rowspan` : Une varias filas en una celda.  

- Ejemplo:

  ```html
  <table border="1">
      <thead>
          <tr>
              <th>X</th>
              <th>Y</th>
          </tr>
      </thead>
      <tbody>
          <tr>
              <td>X1.1</td>
              <td>Y1.2</td>
          </tr>
          <tr>
              <td>X2.1</td>
              <td>Y2.2</td>
          </tr>
      </tbody>
      <tfoot>
          <tr>
              <td colspan="2">Total: 2 registros</td>
          </tr>
      </tfoot>
  </table>```

#### Formularios

- `<form> ... </form>` : Etiqueta principal que define un formulario.

  - Atributos importantes:
    - `action` : Destino donde se enviarán los datos.
    - `method` : Método de envío (`get` o `post`).
    - `name` : Identificador del formulario.

- Campos de entrada (`<input>`)

  - `type="text"` : Campo de texto de una sola línea.
  - `type="password"` : Campo de contraseña.
  - `type="number"` : Campo para valores numéricos.
  - `type="email"` : Campo para direcciones de correo.
  - `type="date"` : Selector de fecha.
  - `type="checkbox"` : Casilla de verificación.
  - `type="radio"` : Botón de opción (agrupados con `name`).
  - `type="submit"` : Botón de envío.
  - `type="reset"` : Botón para reiniciar valores.

- Etiquetas relacionadas

  - `<label>` : Texto asociado a un campo.
  - `<textarea>` : Área de texto multilínea.
  - `<select>` : Lista desplegable.
    - Contiene varias `<option>`.
  - `<fieldset>` : Agrupación de campos.
  - `<legend>` : Título de un grupo de campos.

- Ejemplo:

  ```html
  <form action="procesar.php" method="post">
      <fieldset>
          <legend>Sección A</legend>

          <label for="campo1">Campo 1:</label>
          <input type="text" id="campo1" name="campo1">

          <label for="campo2">Campo 2:</label>
          <input type="number" id="campo2" name="campo2">

          <label>Opción:</label>
          <input type="radio" name="grupo1" value="op1"> A
          <input type="radio" name="grupo1" value="op2"> B
      </fieldset>

      <fieldset>
          <legend>Sección B</legend>

          <label for="campo3">Campo 3:</label>
          <textarea id="campo3" name="campo3"></textarea>

          <label for="campo4">Campo 4:</label>
          <select id="campo4" name="campo4">
              <option value="1">Opción 1</option>
              <option value="2">Opción 2</option>
          </select>
      </fieldset>

      <br>
      <input type="submit" value="Enviar">
      <input type="reset" value="Reiniciar">
  </form>```


#### Multimedia

- **Audio**

  `<audio> ... </audio>` : Reproduce un archivo de audio.  

  - Atributos principales:
    - `src` : Ruta del archivo de audio.  
    - `controls` : Muestra los controles (play, pausa, volumen...).  
    - `autoplay` : Empieza a reproducir automáticamente al cargar la página.  
    - `loop` : Repite el audio de forma indefinida.  
    - `muted` : Comienza en silencio.  

  - Ejemplo:

    ```html
    <audio controls>
        <source src="audio.mp3" type="audio/mpeg">
        <source src="audio.ogg" type="audio/ogg">
        Tu navegador no soporta la etiqueta de audio.
    </audio>
    ```

- **Video**

  `<video> ... </video>` : Reproduce un archivo de vídeo.  

  - Atributos principales:
    - `src` : Ruta del archivo de vídeo.  
    - `controls` : Muestra los controles (play, pausa, volumen, pantalla completa...).  
    - `autoplay` : Reproduce automáticamente.  
    - `loop` : Repite el vídeo indefinidamente.  
    - `muted` : Comienza sin sonido.  
    - `poster` : Imagen mostrada antes de iniciar la reproducción.  
    - `width` / `height` : Tamaño del vídeo en píxeles.  

  - Ejemplo:

    ```html
    <video controls width="320" height="240" poster="imagen.jpg">
        <source src="video.mp4" type="video/mp4">
        <source src="video.ogg" type="video/ogg">
        Tu navegador no soporta la etiqueta de video.
    </video>
    ```

- **Iframe**

  `<iframe> ... </iframe>` : Inserta contenido externo (otra web, mapas, vídeos, etc.).  

  - Atributos principales:
    - `src` : Dirección del contenido a mostrar.  
    - `width` / `height` : Tamaño del iframe.  
    - `title` : Descripción del contenido (accesibilidad).  
    - `frameborder` : Define si hay borde (`0` → sin borde).  
    - `allowfullscreen` : Permite mostrar el contenido en pantalla completa.  

  - Ejemplo:

    ```html
    <iframe src="https://www.ejemplo.com" width="600" height="400" title="contenido externo" frameborder="0"></iframe>
    ```

  - Ejemplo incrustando un vídeo de YouTube:

    ```html
    <iframe width="560" height="315" src="https://www.youtube.com/embed/VIDEO_ID" title="YouTube video"
        frameborder="0" allowfullscreen>
    </iframe>
    ```
