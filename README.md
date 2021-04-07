# Hojas de Estilo en Cascada (CSS)
[Hojas de Estilo en Cascada o CSS](https://www.w3.org/Style/CSS/#specs) (siglas en inglés de *Cascading Style Sheets*) es un lenguaje de diseño gráfico para describir la presentación de un documento escrito en un lenguaje de marcas (ej. HTML). Permite especificar aspectos de diseño como colores, tipos y tamaños de letra, márgenes, alineamientos y muchos otros.

CSS permite manejar la presentación separadamente del contenido, lo que brinda una mayor una flexibilidad en el diseño. Por ejemplo, varios archivos HTML pueden compartir una misma presentación al hacer referencia a un mismo archivo CSS. También posibilita un despliegue diferenciado de acuerdo a los tipos y tamaños de pantallas, en conjunto con HTML5.

Al igual que HTML, CSS es un estándar de W3C. Fue propuesto por Håkon Wium Lie, quien trabajaba en CERN con Tim Berners-Lee, en 1994.

# Ejemplos de aplicación de CSS
- [CSS Zen Garden: The Beauty of CSS Design](http://www.csszengarden.com/)

# Conceptos básicos
## Reglas CSS
Las hojas de estilo se basan en **reglas CSS**, como la que se muestra en la figura 1.

<figure>
  <img src="img/reglacss.png" alt="Selector CSS">
  <figcaption>
    <strong>Figura 1.</strong> Componentes de una regla CSS. Fuente: <a href="https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/CSS_basics">MDN Web Docs</a>.
  </figcaption>
</figure>

Los componentes de una regla CSS son:

1. **El selector**: es el elemento, o elementos HTML, para los que aplica la regla.
2. **La propiedad**: es la característica del elemento HTML (ej. color, tamaño, tipo de letra) a la que se desea aplicar el estilo.
3. **El valor de la propiedad**: es el valor que se le asigna a la propiedad (ej. rojo, azul, etc. para el color).
4. **La declaración**: es la combinación de propiedad y valor de la propiedad.

Entre las llaves (```{}```) pueden especificarse varias declaraciones, las cuales deben separarse con punto y coma (```;```). Aún cuando haya solo una declaración, se recomienda usar el punto y coma, por legibilidad.

Los siguientes son ejemplos de reglas CSS:

```css
p {
    color:red;
}

body {
    background-color:black;
    color:white;
    font-family:Arial;
    margin:0 4px 0 0;
    border:12px solid;
}

h1,h2 {
    color:blue;
    background-color:yellow;
}
```
Pueden encontrarse listas y ejemplos de uso de las propiedades CSS en:
- [CSS Reference - W3 Schools](https://www.w3schools.com/cssref/)
- [CSS Reference - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

### Cómo especificar reglas CSS
Un navegador web busca propiedades CSS en el siguiente orden de prioridad:

1. Elementos HTML (ej. ```body```, ```h1```, ```table```, ...).
2. La sección ```head``` de un documento HTML.
3. Archivos externos (.css).
4. Su configuración por defecto.

#### En elementos HTML
