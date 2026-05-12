# Tipografías Externas y Locales en CSS

Las tipografías son una de las partes más importantes del diseño web.

La tipografía afecta directamente:

- Legibilidad
- Diseño visual
- Identidad visual
- Experiencia del usuario
- Jerarquía del contenido

---

# ¿Qué ocurre por defecto en HTML?

Los navegadores utilizan tipografías predeterminadas.

Por ejemplo:

- Times New Roman
- Arial
- Sans-serif

---

# Problema

Si todos los sitios utilizaran las mismas tipografías:

```txt
Todas las páginas se verían iguales
```

---

# Solución

CSS permite utilizar:

- Tipografías externas
- Tipografías locales
- Tipografías personalizadas

---

# Existen dos formas principales de usar tipografías

| Método | Descripción |
|---|---|
| Google Fonts | Tipografías desde internet |
| Locales | Tipografías descargadas en el proyecto |

---

# Google Fonts

Google Fonts es un servicio gratuito de tipografías web.

Permite:

- Importar fuentes fácilmente
- Utilizar múltiples pesos
- Mejorar diseño visual
- Mantener compatibilidad entre navegadores

---

# Sitio oficial

[Google Fonts](https://fonts.google.com?utm_source=chatgpt.com)

---

# ¿Cómo funciona Google Fonts?

Google almacena las tipografías en sus servidores.

El navegador:

1. Descarga la fuente
2. La carga
3. La aplica visualmente

---

# Flujo general

```txt
Google Fonts → Navegador → Página web
```

---

# Ventajas de Google Fonts

- Fácil implementación
- Gran catálogo
- Optimización automática
- Compatibilidad moderna
- Gratuito

---

# Desventajas

- Depende de internet
- Puede aumentar solicitudes HTTP
- La fuente se descarga externamente

---

# Cómo importar una tipografía desde Google Fonts

---

# Paso 1: Seleccionar fuente

Ejemplo:

```txt
Montserrat
```

---

# Paso 2: Copiar el enlace

Google proporciona un:

```html
<link>
```

---

# Ejemplo

```html
<link
href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap"
rel="stylesheet">
```

---

# Paso 3: Utilizar `font-family`

```css
p {
    font-family: "Montserrat", sans-serif;
}
```

---

# Explicación

| Parte | Función |
|---|---|
| `"Montserrat"` | Fuente principal |
| `sans-serif` | Fuente fallback |

---

# ¿Qué es fallback?

Si la fuente principal falla:

```txt
El navegador utilizará la siguiente
```

---

# Ejemplo

```css
font-family: "Montserrat", sans-serif;
```

---

# Flujo interno

1. Intenta cargar Montserrat
2. Si falla → usa sans-serif

---

# Uso de `preconnect`

Google Fonts suele recomendar:

```html
<link rel="preconnect">
```

---

# Ejemplo

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
```

---

# ¿Qué hace?

Le indica al navegador:

```txt
Prepárate para conectarte a este servidor
```

---

# Beneficio

Puede mejorar ligeramente:

- Rendimiento
- Velocidad de carga

---

# Segundo `preconnect`

```html
<link rel="preconnect"
href="https://fonts.gstatic.com"
crossorigin>
```

---

# ¿Por qué existe `crossorigin`?

Porque la fuente proviene de:

```txt
Otro dominio
```

---

# Ejemplo completo con Google Fonts

## HTML

```html
<link rel="preconnect"
href="https://fonts.googleapis.com">

<link rel="preconnect"
href="https://fonts.gstatic.com"
crossorigin>

<link
href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap"
rel="stylesheet">
```

---

# CSS

```css
body {
    font-family: "Montserrat", sans-serif;
}
```

---

# Tipografías Variables

Algunas fuentes modernas son:

```txt
Variable Fonts
```

---

# ¿Qué significa?

Una sola fuente puede contener:

- Todos los pesos
- Todas las variantes
- Todas las cursivas

---

# Ejemplo

```css
font-weight: 100 900;
```

---

# Ventaja

Reduce:

- Cantidad de archivos
- Solicitudes HTTP

---

# Ejemplo práctico

```css
font-family: "Montserrat", sans-serif;
font-weight: 400;
```

---

# Tipografías Locales

Las tipografías locales son archivos descargados dentro del proyecto.

---

# Flujo

```txt
Proyecto → Carpeta fonts → CSS → Página web
```

---

# Ventajas

- No depende de internet
- Mayor control
- Más privacidad
- Mejor estabilidad

---

# Desventajas

- El proyecto pesa más
- Debes administrar archivos
- Puede aumentar tamaño del repositorio

---

# Formato recomendado

Los formatos más comunes son:

| Formato | Descripción |
|---|---|
| `.ttf` | TrueType Font |
| `.otf` | OpenType Font |
| `.woff` | Web Open Font Format |
| `.woff2` | Más optimizado |

---

# Recomendación moderna

Usar preferiblemente:

```txt
woff2
```

porque es más ligero.

---

# ¿Cómo cargar una fuente local?

Se utiliza:

```css
@font-face
```

---

# ¿Qué es `@font-face`?

Es una regla CSS que permite registrar fuentes personalizadas.

---

# Sintaxis básica

```css
@font-face {
    font-family: "MiFuente";
    src: url("fuente.ttf");
}
```

---

# Explicación

| Propiedad | Función |
|---|---|
| `font-family` | Nombre interno |
| `src` | Ruta del archivo |

---

# Ejemplo completo

```css
@font-face {
    font-family: "Montserrat";

    src: url("fonts/Montserrat.ttf")
    format("truetype");
}
```

---

# ¿Qué hace `format()`?

Le indica al navegador:

```txt
Qué tipo de archivo es
```

---

# Ejemplo

```css
format("truetype")
```

---

# Rutas en fuentes locales

Las rutas pueden ser:

- Relativas
- Absolutas

---

# Ejemplo relativo

```css
src: url("../fonts/fuente.ttf");
```

---

# Ejemplo absoluto

```css
src: url("/fonts/fuente.ttf");
```

---

# Importante

La ruta debe apuntar correctamente al archivo.

Si la ruta falla:

```txt
La fuente no cargará
```

---

# Uso posterior de la fuente

Después de registrar la fuente:

```css
font-family: "Montserrat";
```

---

# Ejemplo

```css
p {
    font-family: "Montserrat";
}
```

---

# Uso de múltiples fuentes locales

Puedes registrar varias fuentes.

---

# Ejemplo

```css
@font-face {
    font-family: "Gloria Hallelujah";
    src: url("Gloria.ttf");
}
```

---

# Uso posterior

```css
h1 {
    font-family: "Gloria Hallelujah";
}
```

---

# Diferencia entre importar y usar

---

# Importar

```css
@font-face
```

o

```html
<link>
```

---

# Usar

```css
font-family
```

---

# Error común de principiantes

Pensar que:

```txt
Importar una fuente automáticamente la aplica
```

---

# Realidad

Primero se importa.

Luego:

```txt
Debe aplicarse con font-family
```

---

# Comparación: Google Fonts vs Local

| Característica | Google Fonts | Local |
|---|---|---|
| Requiere internet | Sí | No |
| Más fácil | Sí | No |
| Control total | No | Sí |
| Rendimiento | Bueno | Depende |
| Privacidad | Menor | Mayor |

---

# ¿Cuál es mejor?

Depende del proyecto.

---

# Google Fonts

Ideal para:

- Aprendizaje
- Proyectos rápidos
- Sitios comunes
- Desarrollo ágil

---

# Fuentes Locales

Ideal para:

- Producción avanzada
- Aplicaciones privadas
- Mayor control
- Mejor independencia

---

# Buenas prácticas

- No usar demasiadas tipografías.
- Mantener consistencia visual.
- Usar máximo 2 o 3 familias.
- Optimizar archivos de fuente.
- Evitar fuentes innecesariamente pesadas.

---

# Error común

Cargar demasiados pesos.

---

# Ejemplo incorrecto

```txt
100 200 300 400 500 600 700 800 900
```

sin necesidad real.

---

# Problema

Aumenta:

- Peso de carga
- Tiempo de renderizado
- Consumo de red

---

# Recomendación profesional

Cargar únicamente:

```txt
Los pesos realmente utilizados
```

---

# Ejemplo optimizado

```txt
400 y 700
```

---

# Propiedad `font-optical-sizing`

Se utiliza en fuentes variables.

---

# Ejemplo

```css
font-optical-sizing: auto;
```

---

# ¿Qué hace?

Permite que el navegador:

```txt
Optimice automáticamente la apariencia visual
```

---

# Compatibilidad

Funciona principalmente con:

```txt
Variable Fonts modernas
```

---

# Ejemplo práctico completo

## HTML

```html
<link
href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap"
rel="stylesheet">
```

---

## CSS

```css
body {
    font-family: "Montserrat", sans-serif;
}
```

---

# Ejemplo completo con fuente local

## CSS

```css
@font-face {
    font-family: "Montserrat";

    src: url("fonts/Montserrat.ttf")
    format("truetype");
}

body {
    font-family: "Montserrat";
}
```

---

# Organización recomendada

```txt
proyecto/
│
├── css/
├── fonts/
├── img/
├── js/
└── index.html
```

---

# ¿Por qué organizar carpetas?

Porque mejora:

- Mantenimiento
- Escalabilidad
- Legibilidad
- Trabajo en equipo

---

# Tabla Conceptual

| Concepto | Función |
|---|---|
| Google Fonts | Tipografías externas |
| @font-face | Registrar fuente local |
| font-family | Aplicar fuente |
| src | Ruta del archivo |
| format() | Tipo de archivo |
| fallback | Fuente alternativa |

---

# Resumen

Las tipografías permiten:

- Mejorar identidad visual
- Mejorar legibilidad
- Crear jerarquías
- Mejorar experiencia de usuario

Comprender correctamente cómo cargar y utilizar tipografías es una parte fundamental del desarrollo frontend moderno.
