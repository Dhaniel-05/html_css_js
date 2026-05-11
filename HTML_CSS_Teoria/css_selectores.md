# Selectores en CSS

Los selectores son uno de los conceptos más importantes de CSS.

Un selector permite indicar:

```txt
Qué elementos HTML serán modificados
```

Sin selectores, CSS no sabría:

- Qué elemento estilizar
- Qué propiedad modificar
- Dónde aplicar los estilos

---

# Relación entre HTML y CSS

HTML crea los elementos.

CSS selecciona esos elementos para aplicar estilos.

---

# Ejemplo básico

## HTML

```html
<h1>Título</h1>
```

## CSS

```css
h1 {
    color: blue;
}
```

Resultado:

```txt
El h1 será azul
```

---

# Sintaxis de un selector

```css
selector {
    propiedad: valor;
}
```

---

# Ejemplo

```css
p {
    color: green;
}
```

---

# Explicación

| Parte | Función |
|---|---|
| `p` | Selector |
| `color` | Propiedad |
| `green` | Valor |

---

# Tipos principales de selectores

Los selectores más importantes para comenzar son:

| Selector | Símbolo |
|---|---|
| Universal | `*` |
| Elemento | `h1`, `p`, `div` |
| Clase | `.` |
| ID | `#` |

---

# Selector Universal

El selector universal selecciona:

```txt
Todos los elementos HTML
```

---

# Sintaxis

```css
* {

}
```

---

# Ejemplo

```css
* {
    margin: 0;
    padding: 0;
}
```

---

# ¿Para qué se utiliza?

Normalmente para:

- Resetear estilos
- Normalizar márgenes
- Configuración global

---

# Ejemplo práctico

```css
* {
    box-sizing: border-box;
}
```

---

# ¿Qué hace `box-sizing`?

Controla cómo CSS calcula:

- Tamaños
- Bordes
- Padding

---

# Selector por Elemento

Selecciona elementos utilizando directamente el nombre de la etiqueta HTML.

---

# Ejemplo

```css
h1 {
    color: blue;
}
```

---

# Resultado

Todos los:

```html
<h1>
```

serán azules.

---

# Ejemplo múltiple

```css
p {
    color: green;
}
```

Todos los párrafos serán verdes.

---

# Ventajas

- Fácil de utilizar.
- Ideal para estilos generales.
- Muy útil en estructuras básicas.

---

# Desventajas

Puede afectar demasiados elementos.

---

# Ejemplo HTML

```html
<h1>Título</h1>

<p>Párrafo</p>
```

---

# Selector por Clase

Las clases permiten agrupar elementos.

Son uno de los selectores más utilizados en desarrollo web.

---

# ¿Qué es una clase?

Es un nombre que se asigna a un elemento utilizando:

```html
class=""
```

---

# Ejemplo HTML

```html
<h2 class="titulo">
    Subtítulo
</h2>
```

---

# Sintaxis CSS

Las clases se seleccionan utilizando:

```txt
.
```

---

# Ejemplo CSS

```css
.titulo {
    color: teal;
}
```

---

# Resultado

Todos los elementos con:

```html
class="titulo"
```

recibirán ese estilo.

---

# Ventaja principal de las clases

Las clases pueden reutilizarse múltiples veces.

---

# Ejemplo

```html
<h2 class="titulo">Título</h2>

<p class="titulo">
    Texto
</p>
```

Ambos compartirán estilos.

---

# Clases y reutilización

Las clases permiten:

- Reutilizar estilos
- Mantener consistencia
- Evitar repetir código

---

# Buenas prácticas para clases

Los nombres deben:

- Ser descriptivos
- Tener sentido
- Explicar el propósito

---

# Incorrecto

```html
class="azul"
```

---

# Mejor

```html
class="boton-principal"
```

---

# ¿Por qué?

Porque describe:

```txt
La función del elemento
```

y no únicamente su apariencia visual.

---

# Clases múltiples

Un elemento puede tener varias clases.

---

# Ejemplo

```html
<p class="texto importante">
```

---

# CSS

```css
.texto {
    font-size: 20px;
}

.importante {
    color: red;
}
```

---

# Resultado

El elemento combinará ambos estilos.

---

# Selector por ID

El selector ID utiliza:

```html
id=""
```

---

# ¿Qué es un ID?

Es un identificador único.

Cada ID debe existir solamente una vez por página.

---

# Ejemplo HTML

```html
<h3 id="subtitulo">
    Identificador único
</h3>
```

---

# Sintaxis CSS

Los IDs se seleccionan utilizando:

```txt
#
```

---

# Ejemplo CSS

```css
#subtitulo {
    color: purple;
}
```

---

# Características importantes del ID

| Característica | Explicación |
|---|---|
| Único | No debe repetirse |
| Alta prioridad | Tiene más peso que clases |
| Identificación específica | Selecciona un único elemento |

---

# Diferencia entre clase e ID

| Clase | ID |
|---|---|
| Reutilizable | Único |
| Usa `.` | Usa `#` |
| Menor prioridad | Mayor prioridad |

---

# ¿Cuándo usar clases?

Cuando varios elementos compartirán estilos.

---

# ¿Cuándo usar IDs?

Cuando un elemento es único.

Por ejemplo:

- Header principal
- Navegación
- Footer
- Formularios específicos

---

# Prioridad de selectores

CSS funciona mediante prioridades.

---

# Prioridad simplificada

| Selector | Prioridad |
|---|---|
| Elemento | Baja |
| Clase | Media |
| ID | Alta |
| Inline | Muy alta |

---

# Ejemplo

```css
p {
    color: blue;
}

.parrafo {
    color: green;
}

#texto {
    color: red;
}
```

---

# HTML

```html
<p id="texto" class="parrafo">
    Texto
</p>
```

---

# Resultado

El texto será:

```txt
Rojo
```

Porque el ID tiene mayor prioridad.

---

# Agrupación de selectores

CSS permite agrupar selectores usando:

```txt
,
```

---

# Ejemplo

```css
h1, p {
    font-family: Arial;
}
```

---

# Ventajas

- Menos código repetido
- Mejor mantenimiento
- Más organización

---

# Ejemplo práctico

```css
#nickname,
#password {
    border: 2px solid gray;
}
```

Ambos elementos compartirán estilos.

---

# Pseudoclases

Las pseudoclases seleccionan elementos según:

- Estado
- Interacción
- Condición

---

# Sintaxis

```css
selector:pseudoclase {

}
```

---

# Ejemplo

```css
input:focus {
    border-color: blue;
}
```

---

# Pseudoclase `:valid`

Selecciona campos válidos.

---

# Ejemplo

```css
input:valid {
    border-color: green;
}
```

---

# ¿Cuándo ocurre?

Cuando el contenido cumple:

- required
- pattern
- minlength
- type

---

# Ejemplo HTML

```html
<input type="email" required>
```

---

# Pseudoclase `:placeholder-shown`

Selecciona inputs que aún muestran placeholder.

---

# Ejemplo

```css
input:placeholder-shown {
    border-color: orange;
}
```

---

# ¿Qué significa?

El input:

- Está vacío
- Aún no tiene contenido

---

# Ejemplo práctico completo

## HTML

```html
<input
    type="text"
    placeholder="Escribe tu nombre"
>
```

---

## CSS

```css
input:placeholder-shown {
    border-color: orange;
}

input:valid {
    border-color: green;
}
```

---

# Resultado visual

| Estado | Color |
|---|---|
| Vacío | Naranja |
| Válido | Verde |

---

# Selectores y jerarquía

CSS también puede seleccionar relaciones entre elementos.

---

# Ejemplo

```css
div p {
    color: blue;
}
```

---

# Significado

Selecciona:

```txt
Todos los p dentro de div
```

---

# HTML

```html
<div>
    <p>Texto azul</p>
</div>
```

---

# Relaciones importantes

| Relación | Ejemplo |
|---|---|
| Padre → Hijo | `div > p` |
| Descendiente | `div p` |
| Hermano | `h1 + p` |

---

# Selector hijo directo

```css
div > p {

}
```

Selecciona únicamente hijos directos.

---

# Selector descendiente

```css
div p {

}
```

Selecciona cualquier `p` dentro de `div`.

---

# Diferencia importante

## Descendiente

```css
div p
```

Busca todos los `p`.

---

## Hijo directo

```css
div > p
```

Solo hijos inmediatos.

---

# CSS moderno depende de selectores

Los selectores son fundamentales para:

- Flexbox
- Grid
- Responsive Design
- Componentes
- Frameworks

---

# Error común de principiantes

Utilizar demasiados IDs.

---

# Recomendación profesional

Usar principalmente:

- Clases
- Selectores semánticos

Los IDs deben utilizarse solo cuando realmente sea necesario.

---

# Buenas prácticas

- Utilizar nombres descriptivos.
- Evitar nombres ambiguos.
- Mantener consistencia.
- Evitar exceso de especificidad.
- Preferir clases sobre IDs.

---

# Ejemplo profesional

## Incorrecto

```html
class="rojo"
```

---

## Correcto

```html
class="boton-error"
```

---

# ¿Por qué?

Porque el diseño visual puede cambiar.

Pero la función del elemento normalmente permanece.

---

# Resumen

| Selector | Símbolo | Uso |
|---|---|---|
| Universal | `*` | Todos los elementos |
| Elemento | `p` | Etiquetas HTML |
| Clase | `.` | Reutilizable |
| ID | `#` | Único |

---

# Prioridad rápida

| Selector | Prioridad |
|---|---|
| Elemento | Baja |
| Clase | Media |
| ID | Alta |
| Inline | Muy alta |

---

# Resumen de pseudoclases

| Pseudoclase | Función |
|---|---|
| `:valid` | Campo válido |
| `:placeholder-shown` | Placeholder visible |
| `:focus` | Elemento enfocado |
| `:hover` | Mouse encima |

---

# Conclusión 

Los selectores permiten:

- Elegir elementos
- Aplicar estilos
- Organizar CSS
- Reutilizar código
- Construir interfaces modernas

Comprender selectores correctamente es una de las bases más importantes de CSS.
