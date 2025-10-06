# CSS

<div align="center">

![CSS](../Images/CSS.png)

</div>

CSS (**Cascading Style Sheets**) es el lenguaje usado para dar estilo y presentación a los documentos HTML.  
Mientras que HTML define la **estructura y el contenido**, CSS se encarga de cómo se verá: colores, tamaños, fuentes, márgenes, posiciones, etc.  

---

## Añadir hojas de estilo a nuestro HTML

Hay **tres formas principales** de aplicar CSS:

1. **En línea (inline):** Se escribe dentro del propio elemento HTML.  
   Poco recomendable porque ensucia el código y dificulta el mantenimiento.

   ```html
   <p style="color: red;">Texto en rojo</p>
   ```

2. **Interno (en el documento):** Se escribe en la etiqueta `<style>` dentro de `<head>`.  
   Útil para proyectos pequeños.

   ```html
   <style>
     p { color: blue; }
   </style>
   ```

3. **Externo (archivo separado):** Guardamos los estilos en un archivo `.css` aparte y lo enlazamos.  
   Es la opción más recomendable.

   ```html
   <link rel="stylesheet" href="estilos.css">
   ```

 **Lo mejor es usar archivos externos para mantener orden y reutilizar código.**

---

## El modelo de caja (Box Model)

En CSS, **todo elemento** se representa como una caja compuesta por:

1. **Contenido:** El texto o imagen que contiene.
2. **Padding (relleno):** Espacio entre el contenido y el borde.
3. **Border (borde):** Línea que rodea el padding y el contenido.
4. **Margin (margen):** Espacio entre el borde del elemento y otros elementos.

Ejemplo visual:

```
┌────────────── Margin ──────────────┐
│ ┌──────────── Border ────────────┐ │
│ │ ┌────────── Padding ─────────┐ │ │
│ │ │        Contenido           │ │ │
│ │ └────────────────────────────┘ │ │
│ └────────────────────────────────┘ │
└────────────────────────────────────┘
```

---

## Etiquetas en línea y en bloque

- **En bloque (block):** Ocupan todo el ancho disponible y comienzan en una nueva línea.  
  Ejemplos: `<div>`, `<h1>`, `<p>`, `<section>`.
  
- **En línea (inline):** Solo ocupan el espacio necesario, no rompen la línea.  
  Ejemplos: `<span>`, `<a>`, `<strong>`, `<img>`.

---

## Selectores CSS

Los **selectores** indican a qué elementos aplicar estilos.

- **Por etiqueta:**  
  Afecta a todos los elementos de ese tipo.

  ```css
  p { color: green; }
  ```

- **Por clase:**  
  Usando un `.` antes del nombre. Se puede reutilizar en varios elementos.  

  ```css
  .destacado { font-weight: bold; }
  /* <h1 class="destacado">Ejemplo </h1>*/
  ```

- **Por id:**  
  Usando `#`. Solo debe usarse en un elemento único (puedes usarlo en los sitios que quieras pero no sería correcto, para ello, usar clases).

  ```css
  #menu { background: lightgray; }
  /* h1 id="menu"> Ejemplo </h1>*/
  ```

- **Combinados:**

  ```css
  div p { color: blue; } /* Todos los <p> dentro de un <div> */
  ```

    ```css
  div, p { color: blue; } /* Todos los <p> y todos los <div> */
  ```

Tener en cuenta que CSS es una hoja de estilos en cascada, por lo tanto, una propiedad más restrictiva tendrá prioridad sobre una más genérica. Por ejemplo:

```css
  div { color: blue; }  /* Color azul para todos los div */
  div p { color: red; } /* Color rojo para todos los p dentro de los div */
  /* Esto es un "conflicto" ya que en ambos modificamos el contenido de un div, pero como, el segundo es más restrictivo,
  nos mostrará azul en todos los div menos el párrafo que saldrá en rojo  */

```

---

## Propiedades interesantes

Algunas de las más comunes:

- **Colores y fondo:** `color`, `background-color`, `background-image`.
- **Texto:** `font-size`, `font-family`, `font-weight`, `text-align`.
- **Cajas:** `margin`, `padding`, `border`, `width`, `height`.
- **Posicionamiento:** `position`, `top`, `left`, `z-index`.
- **Visualización:** `display` (`block`, `inline`, `flex`, `grid`, `none`).
- **Decoración:** `box-shadow`, `border-radius`, `opacity`.

---

## Pseudoselectores

Sirven para aplicar estilos en situaciones **especiales**:

- **De estado:**

  ```css
  a:hover { color: red; }   /* Cuando el ratón pasa por encima */
  input:focus { border: 2px solid blue; } /* Cuando un input está seleccionado */
  ```

- **De posición:**

  ```css
  p:first-child { font-weight: bold; }
  p:last-child { color: gray; }
  ```

- **De condición:**

  ```css
  input:checked { background: yellow; }
  ```

Los pseudoselectores van acompañados **siempre** de un selector, selector:pseudoselector

---

## Estilos por defecto y reseteo

Cada navegador aplica **estilos por defecto** a los elementos (por ejemplo, márgenes en `<body>`).  
Para evitar inconsistencias, se suele usar un **reset CSS** o un **normalize.css**.

Ejemplo de reset básico:

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
```

---

## Prefijos específicos para navegadores

Algunas propiedades nuevas requieren prefijos para funcionar en todos los navegadores:

- `-webkit-` → Chrome, Safari
- `-moz-` → Firefox
- `-o-` → Opera
- `-ms-` → Internet Explorer/Edge antiguo

Ejemplo:

```css
.box {
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  border-radius: 10px;
}
```

---

## Optimización de CSS

Buenas prácticas:

- Usar **archivos externos**.
- Agrupar y reutilizar clases en lugar de repetir código.
- Usar `shorthand` (abreviaciones), por ejemplo:

  ```css
  margin: 10px 20px 15px 5px; /* top, right, bottom, left */
  ```

---

## Herramientas relacionadas con CSS

- **Preprocesadores:** Sass, Less → Añaden variables, funciones y más.
- **Postprocesadores:** PostCSS → Añaden compatibilidad automática.
- **Frameworks:** Bootstrap, Tailwind → Conjuntos de clases listas para usar.
- **DevTools (navegadores):** Herramientas para inspeccionar y probar estilos en vivo.
- **Autoprefixer:** Añade automáticamente los prefijos necesarios.

---
