# Títulos y Párrafos en HTML

Los títulos y párrafos son elementos fundamentales en HTML.

Permiten organizar, estructurar y describir el contenido de una página web.

---

# Títulos o Encabezados

HTML posee 6 niveles de encabezados.

Van desde `<h1>` hasta `<h6>`.

```html
<h1>Título principal</h1>
<h2>Subtítulo</h2>
<h3>Subtítulo</h3>
<h4>Subtítulo</h4>
<h5>Subtítulo</h5>
<h6>Subtítulo</h6>
```

---

# Jerarquía de encabezados

Los encabezados representan niveles de importancia.

| Etiqueta | Nivel |
|---|---|
| `<h1>` | Más importante |
| `<h2>` | Subnivel |
| `<h3>` | Subnivel |
| `<h4>` | Subnivel |
| `<h5>` | Subnivel |
| `<h6>` | Menor importancia |

---

# `<h1>`

Es el encabezado principal de la página.

## Buenas prácticas

- Debe utilizarse una sola vez por página.
- Describe el tema principal del sitio o sección.
- Tiene gran importancia en:
  - SEO
  - Accesibilidad
  - Organización semántica

```html
<h1>Curso de HTML</h1>
```

---

# ¿Por qué es importante el `<h1>`?

Los motores de búsqueda como Google utilizan el `<h1>` para entender de qué trata la página.

Además, tecnologías de asistencia como lectores de pantalla utilizan el `<h1>` como referencia principal del contenido.

Por esta razón:

- Debe ser claro
- Debe describir correctamente la página
- No debe usarse múltiples veces sin necesidad

---

# Encabezados `<h2>` hasta `<h6>`

Se utilizan para subdividir el contenido.

Pueden repetirse las veces necesarias.

```html
<h2>Sección</h2>

<h3>Subsección</h3>
```

---

# Ejemplo de estructura correcta

```html
<h1>Curso de Desarrollo Web</h1>

<h2>HTML</h2>

<h3>Etiquetas básicas</h3>

<h3>Formularios</h3>

<h2>CSS</h2>

<h3>Colores</h3>
```

---

# Error común

Utilizar encabezados únicamente para cambiar tamaños visuales.

Incorrecto:

```html
<h1>Texto grande</h1>
```

Los encabezados representan estructura semántica, NO estilos visuales.

El tamaño visual debe controlarse con CSS.

---

# Emmet para encabezados

Emmet es una herramienta que acelera la escritura de código HTML.

## Crear encabezados automáticamente

```txt
h$*6
```

Genera:

```html
<h1></h1>
<h2></h2>
<h3></h3>
<h4></h4>
<h5></h5>
<h6></h6>
```

---

# Párrafos en HTML

La etiqueta `<p>` se utiliza para crear párrafos.

```html
<p>
    Este es un párrafo.
</p>
```

---

# ¿Qué es un párrafo?

Un párrafo debe contener una idea, concepto o mensaje específico.

Cada párrafo debe tener un propósito dentro del contenido.

---

# Ejemplo conceptual

Incorrecto:

- Hablar de muchos temas distintos en un mismo párrafo.

Correcto:

- Un párrafo para salud física.
- Otro párrafo para salud mental.
- Otro párrafo para alimentación.

---

# Ejemplo de párrafo

```html
<p>
    El ejercicio físico ayuda a mejorar la salud cardiovascular y aumenta la energía diaria.
</p>
```

---

# Buenas prácticas para párrafos

- Mantener una idea principal por párrafo.
- Evitar párrafos excesivamente largos.
- Utilizar lenguaje claro.
- Dividir correctamente la información.

---

# Accesibilidad web

Existen tecnologías de asistencia como:

- Lectores de pantalla
- Navegadores accesibles
- Sistemas de navegación por voz

Estas tecnologías interpretan la estructura semántica del HTML.

Por ejemplo:

- El `<h1>` ayuda a entender el tema principal.
- Los encabezados ayudan a navegar rápidamente por el contenido.
- Los párrafos organizan correctamente la lectura.

---

# Ajuste automático de texto en VS Code

Atajo:

```txt
ALT + Z
```

o

```txt
CTRL + SHIFT + P
```

Permite ajustar automáticamente el contenido a la ventana del editor.

Esto facilita la lectura de párrafos largos.

---

# Diferencia entre semántica y apariencia

HTML define la estructura y significado del contenido.

CSS define la apariencia visual.

## HTML

```html
<h1>Título</h1>
<p>Párrafo</p>
```

## CSS

```css
h1 {
    color: blue;
    font-size: 40px;
}
```

---

# Resumen rápido

| Etiqueta | Función |
|---|---|
| `<h1>` | Título principal |
| `<h2>` | Subtítulo |
| `<h3>` | Subsección |
| `<h4>` | Subnivel |
| `<h5>` | Subnivel |
| `<h6>` | Menor importancia |
| `<p>` | Crear párrafos |
