# Hojas de Estilo en Cascada (CSS)
[Hojas de Estilo en Cascada o CSS](https://www.w3.org/Style/CSS/#specs) (siglas en inglés de *Cascading Style Sheets*) es un lenguaje de diseño gráfico para describir la presentación de un documento escrito en un lenguaje de marcas (ej. HTML). Permite especificar aspectos de diseño como colores, tipos y tamaños de letra, márgenes, alineamientos y muchos otros.

CSS permite manejar la presentación separadamente del contenido, lo que brinda una mayor una flexibilidad en el diseño. Por ejemplo, varios archivos HTML pueden compartir una misma presentación al hacer referencia a un mismo archivo CSS. También posibilita un despliegue diferenciado de acuerdo a los tipos y tamaños de pantallas, en conjunto con HTML5.

Al igual que HTML, CSS es un estándar de W3C. Fue propuesto por Håkon Wium Lie, quien trabajaba en CERN con Tim Berners-Lee, en 1994.

# Ejemplos de uso de CSS
- [CSS Zen Garden: The Beauty of CSS Design](http://www.csszengarden.com/)
- [En CodePen: Intro Front-End Holy Trinity](https://codepen.io/mongeauc/pen/gPVoXd)

# Conceptos básicos
## Reglas CSS
Las hojas de estilo se basan en **reglas CSS**, como la que se muestra en la figura 1.

<figure>
  <img src="img/reglacss.png" alt="Selector CSS" />
  <figcaption>
    <strong>Figura 1.</strong> Componentes de una regla CSS. Fuente: <a href="https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/CSS_basics">MDN Web Docs.</a>
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
- [CSS Reference - MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)
- [CSS Reference - W3 Schools](https://www.w3schools.com/cssref/)


### Cómo especificar reglas y propiedades CSS
Un navegador web busca reglas y propiedades CSS en el siguiente orden de prioridad:

1. En elementos HTML individuales (ej. ```body```, ```h1```, ```table```, ...).
2. En el elemento ```style```.
3. En archivos CSS (.css).
4. En su configuración por defecto.

#### En elementos HTML individuales
Se hace a través del atributo global [style](https://developer.mozilla.org/es/docs/Web/HTML/Global_attributes/style), como en el siguiente ejemplo:

```html
<h1 style="color:blue;">Encabezado estilizado</h1>
```

Esta forma no separa el contenido del estilo por lo que, en general, no es recomendada.

#### En el elemento ```style```

El elemento [style](https://developer.mozilla.org/es/docs/Web/HTML/Element/style) se ubica, por lo general, dentro del elemento ```head```.

```html
<head>
    <title>Ejemplo de reglas CSS especificadas en el elemento <style></title>
    <style>
        h1 {
            color:blue;
        }
    </style>
</head>
```

#### En archivos CSS (.css)
En la sección ```head``` del archivo HTML que va a usar los estilos, debe incluirse un elemento de tipo [link](https://developer.mozilla.org/es/docs/Web/HTML/Element/link), como se ejemplifica seguidamente:

```html
<link rel="stylesheet" href="css/estilos.css">
```

Ejemplo de contenido de ```css/estilos.css```:

```css
p {
    color:red;
    font-size:200%;
}

h1 {
    background-color:yellow;
}  

body {
    background-color:black;
    color:white;
    margin:0 4px 0 0;
    border:12px solid;
}
```

# Ejercicios
1. Con base en la [tarea 01](https://tpb729-desarrollosigweb-2021.github.io/tarea-01-html/), construya un sitio web, con varias páginas, sobre los felinos de Costa Rica.  
a. Cree un archivo llamado *index.html* con información general sobre los felinos de Costa Rica (puede usar el de la tarea).  
b. Cree un archivo llamado *panhera-onca.html* con información sobre esa especie. Incluya, al menos, el título, un encabezado, un párrafo y una imagen (sugerencia: use contenido de Wikipedia).  
c. Cree un archivo llamado *css/estilos.css* que, para ambos archivos, especifique mediante CSS, por lo menos: el tipo y tamaño de letra, el color de fondo y el color de los encabezados.  
d. Cree un archivo llamado *puma-concolor.html* con información sobre esa especie. Incluya, al menos, el título, un encabezado, un párrafo y una imagen (sugerencia: use contenido de Wikipedia). Aplique aquí también los estilos de *css/estilos.css*.  
e. En cada página, cree una barra de navegación que permita navegar a las otras dos páginas. Para esto utilice el elemento [nav](https://developer.mozilla.org/es/docs/Web/HTML/Element/nav).  
