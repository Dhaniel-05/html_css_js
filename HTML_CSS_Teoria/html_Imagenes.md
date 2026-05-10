# Imágenes en HTML

Las imágenes permiten representar contenido visual dentro de una página web.

Se utilizan para:

- Logotipos
- Fotografías
- Íconos
- Ilustraciones
- Productos
- Banners
- Recursos visuales

---

# La etiqueta `<img>`

La etiqueta `<img>` se utiliza para insertar imágenes en HTML.

```html
<img src="imagen.png">
```

---

# Características de `<img>`

La etiqueta `<img>` es:

- Una etiqueta de línea
- Un elemento vacío
- Una etiqueta autocerrada

No necesita etiqueta de cierre.

Incorrecto:

```html
<img></img>
```

Correcto:

```html
<img src="imagen.png">
```

---

# ¿Qué es una Self Closing Tag?

Son etiquetas que se autocierran automáticamente.

Ejemplos:

```html
<img>
<br>
<hr>
<input>
<meta>
```

---

# Estructura básica de una imagen

```html
<img 
    src="imagen.png"
    alt="Descripción de la imagen"
>
```

---

# Atributo `src`

`src` significa:

```txt
Source
```

Define la ruta o ubicación de la imagen.

```html
<img src="imagen.png">
```

---

# Imágenes locales

Son imágenes almacenadas dentro del proyecto.

---

# Ejemplo

```html
<img src="logo.png">
```

---

# Ejemplo con carpetas

```html
<img src="img/logo.png">
```

---

# Organización recomendada

```txt
proyecto/
│
├── index.html
│
└── img/
    ├── logo.png
    └── banner.jpg
```

---

# Imágenes externas

También es posible cargar imágenes desde internet.

---

# Ejemplo

```html
<img src="https://pagina.com/imagen.jpg">
```

---

# Diferencia entre imagen local y externa

| Tipo | Ubicación |
|---|---|
| Local | Dentro del proyecto |
| Externa | Desde internet |

---

# Ventajas de imágenes locales

- Mayor control
- Más velocidad
- No depende de terceros
- Más estabilidad

---

# Desventajas de imágenes externas

- Pueden dejar de funcionar
- Dependencia del servidor externo
- Posibles problemas de rendimiento

---

# Atributo `alt`

`alt` significa:

```txt
Alternative Text
```

Proporciona una descripción textual de la imagen.

```html
<img 
    src="logo.png"
    alt="Logotipo de HTML5"
>
```

---

# ¿Por qué es importante `alt`?

El atributo `alt` es fundamental para:

- Accesibilidad web
- Lectores de pantalla
- SEO
- Fallback cuando la imagen falla

---

# ¿Qué ocurre si la imagen no carga?

Si la imagen falla, el navegador mostrará el contenido de `alt`.

---

# Ejemplo

```html
<img 
    src="imagen-no-existe.png"
    alt="Imagen de ejemplo"
>
```

---

# Buenas prácticas para `alt`

Correcto:

```html
alt="Logotipo de HTML5"
```

Incorrecto:

```html
alt="imagen"
```

El texto alternativo debe ser:

- Claro
- Descriptivo
- Corto
- Útil

---

# Ejemplos de `alt`

| Imagen | Alt recomendado |
|---|---|
| Logo | `"Logotipo de la empresa"` |
| Paisaje | `"Montañas y lago al atardecer"` |
| Producto | `"Zapatos deportivos negros"` |

---

# Atributo `title`

Muestra un tooltip cuando el usuario pasa el mouse sobre la imagen.

```html
<img 
    src="logo.png"
    title="HTML5"
>
```

---

# Diferencia entre `alt` y `title`

| Atributo | Función |
|---|---|
| `alt` | Descripción accesible |
| `title` | Información adicional visual |

---

# Atributos `width` y `height`

Permiten definir el tamaño de la imagen.

```html
<img 
    src="logo.png"
    width="200"
    height="200"
>
```

---

# Importante sobre tamaños

Aunque HTML permite modificar tamaños, normalmente el control visual se realiza con CSS.

HTML:

```html
<img src="logo.png" width="200">
```

CSS:

```css
img {
    width: 200px;
}
```

---

# Ejemplo completo

```html
<img 
    src="logo-html.png"
    alt="Logotipo de HTML5"
    title="HTML5"
    width="200"
    height="200"
>
```

---

# Etiquetas de bloque y etiquetas de línea

La etiqueta `<img>` es un elemento de línea.

Esto significa que puede compartir espacio con otros elementos en la misma línea.

---

# Ejemplo

```html
<img src="logo.png">
<img src="logo2.png">
```

---

# Formatos de imágenes comunes

| Formato | Uso |
|---|---|
| `.png` | Transparencias |
| `.jpg` / `.jpeg` | Fotografías |
| `.gif` | Animaciones |
| `.svg` | Gráficos vectoriales |
| `.webp` | Mejor optimización web |

---

# ¿Qué es SVG?

SVG significa:

```txt
Scalable Vector Graphics
```

Son imágenes vectoriales que NO pierden calidad al escalarse.

Muy utilizadas en:

- Logos
- Íconos
- Interfaces

---

# Error común

Incorrecto:

```html
<img>
```

Correcto:

```html
<img src="imagen.png" alt="Descripción">
```

La imagen necesita al menos:

- `src`
- `alt`

---

# Accesibilidad en imágenes

Los lectores de pantalla utilizan `alt` para describir imágenes a personas con discapacidad visual.

Por eso:

- Nunca debe omitirse `alt`
- Debe describir correctamente la imagen

---

# Imágenes decorativas

Si la imagen es únicamente decorativa:

```html
<img src="decoracion.png" alt="">
```

En este caso el `alt` queda vacío para que los lectores de pantalla la ignoren.

---

# Enlazar imágenes

Las imágenes también pueden funcionar como enlaces.

```html
<a href="https://google.com">
    <img src="logo.png" alt="Google">
</a>
```

---

# Lazy Loading

Permite cargar imágenes solo cuando son necesarias.

Mejora el rendimiento de la página.

```html
<img 
    src="imagen.jpg"
    alt="Paisaje"
    loading="lazy"
>
```

---

# Beneficios de `loading="lazy"`

- Mejora rendimiento
- Reduce consumo de datos
- Acelera carga inicial

---

# Emmet para imágenes

## Crear imagen rápida

```txt
img
```

Genera:

```html
<img src="" alt="">
```

---

# Buenas prácticas generales

- Utilizar nombres descriptivos.
- Optimizar tamaños.
- Utilizar `alt`.
- Evitar imágenes excesivamente pesadas.
- Organizar imágenes en carpetas.
- Preferir formatos modernos como `.webp`.

---

# Resumen rápido

| Atributo | Función |
|---|---|
| `src` | Ruta de la imagen |
| `alt` | Texto alternativo |
| `title` | Tooltip |
| `width` | Ancho |
| `height` | Alto |
| `loading="lazy"` | Carga diferida |

---

# Resumen de etiquetas

| Etiqueta | Función |
|---|---|
| `<img>` | Insertar imagen |
| `<a>` | Crear enlace |
