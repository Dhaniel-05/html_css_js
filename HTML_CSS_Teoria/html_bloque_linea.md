# Elementos de Bloque e Inline en HTML

En HTML, los elementos tienen diferentes comportamientos visuales.

Los dos comportamientos principales son:

- Elementos de bloque
- Elementos en línea

Comprender esta diferencia es fundamental para aprender:

- Maquetación web
- CSS
- Flexbox
- Grid
- Responsive Design

---

# Flujo normal del documento

HTML organiza los elementos siguiendo un flujo natural.

Los elementos pueden:

- Ocupar toda una línea
- Compartir espacio en la misma línea

Aquí es donde aparecen los conceptos:

- `block`
- `inline`

---

# Elementos de Bloque

Los elementos de bloque ocupan todo el ancho disponible de su contenedor.

Siempre comienzan en una nueva línea.

---

# Comportamiento visual

```txt
[BLOQUE]
[BLOQUE]
[BLOQUE]
```

Se apilan verticalmente.

---

# Características de los elementos block

- Ocupan todo el ancho disponible.
- Generan salto de línea automáticamente.
- Se colocan uno debajo del otro.
- Pueden contener elementos inline y otros block.
- Permiten modificar:
  - width
  - height
  - margin
  - padding

---

# Ejemplo básico

```html
<div>Bloque 1</div>

<div>Bloque 2</div>
```

Resultado visual:

```txt
Bloque 1
Bloque 2
```

---

# Etiquetas block comunes

| Etiqueta | Función |
|---|---|
| `<div>` | Contenedor genérico |
| `<p>` | Párrafo |
| `<h1>` - `<h6>` | Encabezados |
| `<section>` | Sección |
| `<article>` | Artículo |
| `<header>` | Encabezado |
| `<footer>` | Pie de página |
| `<nav>` | Navegación |
| `<ul>` | Lista |
| `<ol>` | Lista ordenada |

---

# Ejemplo visual con estilos

```html
<div style="background:red;">
    Bloque 1
</div>

<div style="background:blue;">
    Bloque 2
</div>
```

Cada elemento ocupará una línea completa.

---

# Elementos Inline

Los elementos inline solo ocupan el espacio necesario para su contenido.

NO generan saltos de línea automáticamente.

---

# Comportamiento visual

```txt
Texto [INLINE] Texto [INLINE]
```

Permanecen en la misma línea.

---

# Características de los elementos inline

- Solo ocupan el ancho de su contenido.
- NO generan salto de línea.
- Fluyen junto al texto.
- No ocupan todo el ancho disponible.
- Se utilizan normalmente dentro de textos.

---

# Ejemplo básico

```html
<span>Inline 1</span>
<span>Inline 2</span>
```

Resultado visual:

```txt
Inline 1 Inline 2
```

---

# Etiquetas inline comunes

| Etiqueta | Función |
|---|---|
| `<span>` | Contenedor inline |
| `<a>` | Enlace |
| `<strong>` | Texto importante |
| `<em>` | Énfasis |
| `<img>` | Imagen |
| `<label>` | Etiqueta descriptiva |
| `<code>` | Código |
| `<small>` | Texto pequeño |

---

# Ejemplo visual

```html
<p>
    Texto normal
    <span style="background:lightblue;">
        Inline
    </span>
    texto normal.
</p>
```

El `span` permanece dentro del flujo del texto.

---

# Diferencia principal

| Block | Inline |
|---|---|
| Ocupa toda la línea | Solo ocupa su contenido |
| Genera salto de línea | No genera salto |
| Se apila verticalmente | Permanece en línea |
| Puede contener inline y block | Generalmente contiene texto |

---

# Comparación visual

## Elementos block

```txt
[BLOCK]
[BLOCK]
[BLOCK]
```

---

## Elementos inline

```txt
[INLINE] [INLINE] [INLINE]
```

---

# Ejemplo práctico completo

```html
<div>
    Soy un elemento block.
</div>

<span>
    Soy inline.
</span>

<span>
    También soy inline.
</span>
```

Resultado:

```txt
Soy un elemento block.

Soy inline. También soy inline.
```

---

# Contenedores genéricos

HTML tiene dos contenedores principales:

| Etiqueta | Tipo |
|---|---|
| `<div>` | Block |
| `<span>` | Inline |

---

# `<div>`

Es un contenedor de bloque.

Muy utilizado para:

- Estructuras
- Layouts
- Secciones
- Componentes

```html
<div>
    Contenido
</div>
```

---

# `<span>`

Es un contenedor inline.

Muy utilizado para:

- Resaltar texto
- Aplicar estilos específicos
- Modificar pequeñas partes del contenido

```html
<span>
    Texto resaltado
</span>
```

---

# Error común

Incorrecto:

```html
<p>
    Texto
    <div>Bloque dentro de párrafo</div>
</p>
```

---

# ¿Por qué es incorrecto?

La etiqueta `<p>` NO debe contener elementos block como `<div>`.

Esto rompe la estructura semántica del documento.

---

# Correcto

```html
<div>
    <p>Texto</p>
</div>
```

---

# CSS y display

CSS puede cambiar el comportamiento de los elementos.

---

# Convertir block a inline

```css
div {
    display: inline;
}
```

---

# Convertir inline a block

```css
span {
    display: block;
}
```

---

# Tipos de display más comunes

| Valor | Función |
|---|---|
| `block` | Elemento de bloque |
| `inline` | Elemento en línea |
| `inline-block` | Mezcla de ambos |
| `flex` | Flexbox |
| `grid` | CSS Grid |
| `none` | Oculta elemento |

---

# ¿Qué es `inline-block`?

Permite que un elemento:

- Permanezca en línea
- Pero acepte tamaños (`width` y `height`)

---

# Ejemplo

```css
span {
    display: inline-block;
    width: 200px;
}
```

---

# Diferencia entre inline e inline-block

| Inline | Inline-block |
|---|---|
| No acepta width/height correctamente | Sí acepta |
| Solo depende del contenido | Puede tener tamaño personalizado |

---

# Importancia en desarrollo web

Comprender block e inline es esencial para:

- Diseñar interfaces
- Organizar contenido
- Crear layouts
- Entender CSS
- Trabajar con Flexbox y Grid

---

# Accesibilidad y semántica

La elección correcta de etiquetas mejora:

- Lectura del código
- Organización
- SEO
- Accesibilidad

---

# Ejemplo semántico correcto

```html
<section>
    <h2>Título</h2>

    <p>
        Texto con un
        <span>fragmento resaltado</span>.
    </p>
</section>
```

---

# Buenas prácticas

- Utilizar block para estructuras grandes.
- Utilizar inline para pequeños fragmentos.
- Mantener semántica correcta.
- No usar etiquetas incorrectas solo por apariencia visual.
- Controlar estilos visuales con CSS.

---

# Resumen rápido

| Tipo | Característica principal |
|---|---|
| Block | Ocupa toda la línea |
| Inline | Solo ocupa su contenido |

---

# Resumen de etiquetas

| Etiqueta | Tipo |
|---|---|
| `<div>` | Block |
| `<p>` | Block |
| `<section>` | Block |
| `<h1>` | Block |
| `<ul>` | Block |
| `<span>` | Inline |
| `<a>` | Inline |
| `<strong>` | Inline |
| `<em>` | Inline |
| `<img>` | Inline |
