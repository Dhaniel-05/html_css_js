# Estructura básica de HTML

Todo documento HTML tiene una estructura base que el navegador utiliza para interpretar correctamente la página web.

---

# Estructura básica

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

---

# `<!DOCTYPE html>`

Indica al navegador que el documento utiliza HTML5.

Debe colocarse siempre en la primera línea del documento.

```html
<!DOCTYPE html>
```

---

# `<html>`

Es la etiqueta raíz del documento HTML.

Todo el contenido de la página debe ir dentro de esta etiqueta.

```html
<html lang="en">
</html>
```

---

## Atributo `lang`

Define el idioma principal de la página.

Ejemplo:

```html
<html lang="es">
```

### Algunos valores comunes

| Valor | Idioma |
|---|---|
| `es` | Español |
| `en` | Inglés |
| `fr` | Francés |
| `pt` | Portugués |

---

# `<head>`

Contiene configuraciones internas del documento.

La información dentro de `<head>` normalmente NO es visible directamente en la página.

```html
<head>
</head>
```

---

# Elementos comunes dentro de `<head>`

- Meta etiquetas
- Título de la página
- Archivos CSS
- Scripts JavaScript
- Configuraciones SEO

---

# `<meta charset="UTF-8">`

Permite utilizar caracteres especiales correctamente.

Ejemplos:

- á
- é
- í
- ó
- ú
- ñ

```html
<meta charset="UTF-8">
```

---

# `<meta name="viewport">`

Hace que la página sea responsive en dispositivos móviles.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

## Explicación

| Propiedad | Función |
|---|---|
| `width=device-width` | Ajusta el ancho al dispositivo |
| `initial-scale=1.0` | Define el nivel de zoom inicial |

---

# `<title>`

Define el título de la página.

Este título aparece:

- En la pestaña del navegador
- En favoritos
- En motores de búsqueda

```html
<title>Document</title>
```

---

# `<body>`

Contiene todo el contenido visible de la página web.

```html
<body>

</body>
```

---

# Elementos que normalmente van dentro de `<body>`

- Títulos
- Párrafos
- Imágenes
- Formularios
- Botones
- Tablas
- Videos
- Enlaces

---

# Estructura visual básica

```txt
Documento HTML
│
├── <!DOCTYPE html>
│
└── <html>
    │
    ├── <head>
    │   ├── meta
    │   ├── title
    │   └── configuraciones
    │
    └── <body>
        └── contenido visible
```

---

# Buenas prácticas

- Utilizar siempre `<!DOCTYPE html>`
- Definir correctamente el idioma con `lang`
- Agregar `meta charset="UTF-8"`
- Utilizar `viewport` para responsive design
- Mantener organizado el código
- Utilizar indentación correcta

---

# Resumen

| Etiqueta | Función |
|---|---|
| `<!DOCTYPE html>` | Define HTML5 |
| `<html>` | Contenedor principal |
| `<head>` | Configuración interna |
| `<meta>` | Metadatos |
| `<title>` | Título de la página |
| `<body>` | Contenido visible |
