# Propiedades de Texto en CSS

CSS permite modificar completamente la apariencia del texto.

Las propiedades de texto son fundamentales porque:

- Mejoran la legibilidad
- Mejoran la accesibilidad
- Mejoran el diseño visual
- Ayudan a crear jerarquías visuales
- Facilitan la experiencia del usuario

---

# Relación entre HTML y CSS

HTML crea el contenido.

CSS modifica la apariencia visual de ese contenido.

---

# Ejemplo HTML

```html
<h1>Propiedades de Texto</h1>

<p>
    Lorem <strong>ipsum</strong> dolor sit amet.
</p>

<a href="#">
    Enlace
</a>
```

---

# La etiqueta `<strong>`

La etiqueta:

```html
<strong>
```

se utiliza para dar:

```txt
Importancia semántica al texto
```

---

# Ejemplo

```html
<p>
    Este texto es <strong>importante</strong>
</p>
```

---

# Resultado

El navegador normalmente mostrará el texto:

- En negrita
- Con mayor énfasis visual

---

# Importante

`<strong>` NO existe solamente para poner texto en negrita.

También indica:

```txt
Importancia semántica
```

---

# Beneficios de `<strong>`

- Mejor accesibilidad
- Mejor comprensión para lectores de pantalla
- Puede ayudar al SEO
- Mejora la semántica HTML

---

# ¿Qué son las propiedades de texto?

Son propiedades CSS que modifican:

- Fuente
- Tamaño
- Grosor
- Espaciado
- Decoración
- Transformación
- Alineación

---

# Sintaxis básica

```css
selector {
    propiedad: valor;
}
```

---

# Ejemplo

```css
p {
    color: gray;
}
```

---

# Propiedad `font-family`

Define la tipografía del texto.

---

# Ejemplo

```css
h1 {
    font-family: Arial;
}
```

---

# Tipografías y fallback

Es recomendable colocar varias fuentes.

---

# Ejemplo

```css
p {
    font-family: Arial, Helvetica, sans-serif;
}
```

---

# ¿Cómo funciona?

CSS prueba las fuentes:

```txt
De izquierda a derecha
```

---

# Explicación

1. Intenta cargar Arial.
2. Si no existe, usa Helvetica.
3. Si tampoco existe, usa cualquier sans-serif.

---

# ¿Qué significa `sans-serif`?

Es una familia genérica de tipografía.

---

# Familias genéricas comunes

| Familia | Descripción |
|---|---|
| `serif` | Letras con adornos |
| `sans-serif` | Letras modernas sin adornos |
| `monospace` | Todas las letras ocupan el mismo espacio |
| `cursive` | Estilo manuscrito |
| `fantasy` | Decorativas |

---

# Ejemplo visual

```css
font-family: monospace;
```

Se utiliza mucho en:

- Código
- Terminales
- Consolas

---

# Fuentes con espacios

Cuando una tipografía tiene espacios:

```txt
Debe ir entre comillas
```

---

# Ejemplo

```css
font-family: 'Lucida Sans';
```

---

# Propiedad `font-size`

Controla el tamaño del texto.

---

# Ejemplo

```css
p {
    font-size: 16px;
}
```

---

# Unidades comunes

| Unidad | Descripción |
|---|---|
| `px` | Píxeles |
| `em` | Relativa al padre |
| `rem` | Relativa al root |
| `%` | Porcentaje |

---

# Ejemplo

```css
h1 {
    font-size: 2em;
}
```

---

# Recomendación moderna

Usar preferiblemente:

- `rem`
- `em`

Porque son más adaptables.

---

# Propiedad `color`

Modifica el color del texto.

---

# Ejemplo

```css
p {
    color: blue;
}
```

---

# Formas de definir colores

| Forma | Ejemplo |
|---|---|
| Nombre | `blue` |
| Hexadecimal | `#0000ff` |
| RGB | `rgb(0,0,255)` |
| RGBA | `rgba(0,0,255,0.5)` |

---

# ¿Qué significa RGBA?

| Valor | Significado |
|---|---|
| R | Red |
| G | Green |
| B | Blue |
| A | Alpha (transparencia) |

---

# Ejemplo

```css
color: rgba(0, 0, 255, 0.5);
```

---

# Propiedad `font-weight`

Controla el grosor del texto.

---

# Ejemplo

```css
p {
    font-weight: bold;
}
```

---

# Escala de pesos

CSS utiliza valores:

```txt
100 → 900
```

---

# Tabla de pesos

| Valor | Grosor |
|---|---|
| 100 | Muy fino |
| 300 | Ligero |
| 400 | Normal |
| 700 | Bold |
| 900 | Muy grueso |

---

# Ejemplo

```css
font-weight: 700;
```

---

# `bold` vs `bolder`

## `bold`

Aplica normalmente:

```txt
700
```

---

## `bolder`

Hace el texto:

```txt
Más grueso que el padre
```

---

# Importante

No todas las fuentes soportan todos los pesos.

---

# Ejemplo

Algunas tipografías solo tienen:

- 400
- 700

Por lo tanto:

```txt
500 o 600 podrían verse iguales
```

---

# Propiedad `font-style`

Controla el estilo de la fuente.

---

# Valores comunes

| Valor | Función |
|---|---|
| `normal` | Texto normal |
| `italic` | Cursiva |
| `oblique` | Texto inclinado |

---

# Ejemplo

```css
p {
    font-style: italic;
}
```

---

# Uso recomendado

La cursiva suele utilizarse para:

- Énfasis
- Citas
- Palabras extranjeras

---

# Propiedad `text-align`

Controla la alineación del texto.

---

# Valores principales

| Valor | Función |
|---|---|
| `left` | Izquierda |
| `center` | Centro |
| `right` | Derecha |
| `justify` | Justificado |

---

# Ejemplo

```css
h1 {
    text-align: center;
}
```

---

# Importante

`text-align` funciona principalmente sobre:

```txt
Elementos de bloque
```

---

# ¿Por qué?

Porque los bloques ocupan ancho completo.

---

# Ejemplo

```html
<h1>Título</h1>
```

El `h1` ocupa todo el ancho disponible.

---

# ¿Qué ocurre con elementos inline?

Los elementos inline:

- No ocupan todo el ancho
- Solo ocupan el espacio del contenido

Por eso:

```txt
text-align muchas veces no tiene efecto visible
```

---

# Justificado (`justify`)

Distribuye el texto uniformemente.

---

# Ejemplo

```css
p {
    text-align: justify;
}
```

---

# Resultado

Las líneas comienzan y terminan alineadas.

Similar a:

- Word
- Libros
- Periódicos

---

# Propiedad `text-decoration`

Controla decoraciones del texto.

---

# Valores comunes

| Valor | Función |
|---|---|
| `none` | Sin decoración |
| `underline` | Subrayado |
| `line-through` | Tachado |
| `overline` | Línea superior |

---

# Ejemplo

```css
a {
    text-decoration: none;
}
```

---

# ¿Por qué se usa mucho en enlaces?

Porque los navegadores:

```txt
Subrayan los enlaces por defecto
```

---

# Propiedad `line-height`

Controla el espacio vertical entre líneas.

---

# Ejemplo

```css
p {
    line-height: 1.5;
}
```

---

# Beneficios

- Mejora legibilidad
- Evita texto amontonado
- Facilita lectura

---

# Recomendación común

```css
line-height: 1.5;
```

o

```css
line-height: 1.6;
```

---

# Importante

Un line-height muy pequeño:

```txt
Dificulta la lectura
```

---

# Propiedad `letter-spacing`

Controla el espacio entre letras.

---

# Ejemplo

```css
a {
    letter-spacing: 5px;
}
```

---

# Resultado

Las letras estarán más separadas.

---

# Uso recomendado

Utilizar con moderación.

---

# Problema común

Mucho espacio entre letras puede:

- Dificultar lectura
- Romper la estética
- Cansar visualmente

---

# Propiedad `text-transform`

Transforma visualmente el texto.

---

# Valores comunes

| Valor | Resultado |
|---|---|
| `uppercase` | MAYÚSCULAS |
| `lowercase` | minúsculas |
| `capitalize` | Primera Letra |

---

# Ejemplo

```css
a {
    text-transform: capitalize;
}
```

---

# Resultado

```txt
hola mundo
```

se verá como:

```txt
Hola Mundo
```

---

# Importante

`text-transform`:

```txt
NO cambia el contenido original
```

Solo modifica:

```txt
La representación visual
```

---

# Propiedades comunes en enlaces

Los enlaces suelen modificar:

- text-decoration
- color
- font-family
- letter-spacing
- text-transform

---

# Ejemplo completo

```css
a {
    text-decoration: none;
    color: teal;
    font-family: monospace;
    letter-spacing: 2px;
}
```

---

# Herencia en CSS

Muchas propiedades de texto:

```txt
Se heredan automáticamente
```

---

# Ejemplo

```css
body {
    font-family: Arial;
}
```

Todos los hijos heredarán esa fuente.

---

# Ventaja

Evita repetir código.

---

# Ejemplo práctico completo

## HTML

```html
<h1>Título</h1>

<p>
    Texto de ejemplo
</p>

<a href="#">
    Enlace
</a>
```

---

## CSS

```css
h1 {
    font-family: Arial;
    text-align: center;
    color: teal;
}

p {
    font-size: 16px;
    line-height: 1.5;
    color: gray;
}

a {
    text-decoration: none;
    letter-spacing: 2px;
}
```

---

# Tipografía y experiencia de usuario

La tipografía afecta:

- Legibilidad
- Accesibilidad
- Diseño
- Navegación
- Comprensión visual

---

# Error común de principiantes

Usar demasiadas fuentes distintas.

---

# Recomendación profesional

Utilizar:

```txt
2 o máximo 3 tipografías
```

en un mismo proyecto.

---

# Jerarquía visual

CSS permite crear jerarquías utilizando:

- Tamaño
- Grosor
- Color
- Espaciado

---

# Ejemplo

```css
h1 {
    font-size: 40px;
}

p {
    font-size: 16px;
}
```

---

# Resultado

El usuario entiende inmediatamente:

```txt
Qué contenido es más importante
```

---

# Buenas prácticas

- Mantener buena legibilidad.
- No abusar de cursivas.
- No abusar de mayúsculas.
- Usar line-height adecuado.
- Utilizar pocas tipografías.
- Mantener consistencia visual.

---

# Condensado

| Propiedad | Función |
|---|---|
| `font-family` | Tipografía |
| `font-size` | Tamaño |
| `font-weight` | Grosor |
| `font-style` | Cursiva |
| `color` | Color |
| `text-align` | Alineación |
| `text-decoration` | Decoración |
| `line-height` | Espacio entre líneas |
| `letter-spacing` | Espacio entre letras |
| `text-transform` | Transformación visual |

---

# Resumen 

Las propiedades de texto son fundamentales porque permiten:

- Mejorar diseño
- Mejorar lectura
- Crear jerarquías visuales
- Mejorar accesibilidad
- Construir interfaces profesionales

Comprender tipografía en CSS es una de las bases más importantes del diseño web moderno.
