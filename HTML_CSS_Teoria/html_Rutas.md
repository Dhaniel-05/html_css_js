# Rutas Absolutas y Relativas en HTML

Las rutas permiten localizar recursos dentro o fuera de un proyecto web.

Los recursos pueden ser:

- Páginas HTML
- Imágenes
- Videos
- Archivos CSS
- Archivos JavaScript
- Documentos
- Audios

---

# ¿Qué es una ruta?

Una ruta es la dirección que HTML utiliza para encontrar un recurso.

Por ejemplo:

```html
<img src="logo.png">
```

La ruta indica dónde se encuentra `logo.png`.

---

# Tipos de rutas

Existen dos tipos principales:

| Tipo | Descripción |
|---|---|
| Ruta absoluta | Dirección completa |
| Ruta relativa | Dirección basada en el proyecto |

---

# Rutas Absolutas

Las rutas absolutas utilizan la dirección completa del recurso.

Normalmente apuntan a:

- Sitios externos
- Recursos en internet
- Servidores remotos

---

# Ejemplo

```html
<a href="https://www.google.com">
    Google
</a>
```

---

# Imagen externa

```html
<img 
    src="https://www.manualweb.net/img/covers/html5-cover.jpg"
    alt="Portada HTML5"
>
```

---

# Características de las rutas absolutas

- Utilizan URL completa.
- Funcionan desde cualquier ubicación.
- Dependen de internet.
- Apuntan normalmente a servidores externos.

---

# Estructura de una ruta absoluta

```txt
https://dominio.com/carpeta/archivo.html
```

---

# Partes de una URL

| Parte | Función |
|---|---|
| `https://` | Protocolo |
| `dominio.com` | Dominio |
| `/carpeta/` | Directorio |
| `archivo.html` | Archivo |

---

# Protocolos comunes

| Protocolo | Uso |
|---|---|
| `https://` | Web segura |
| `http://` | Web no segura |
| `mailto:` | Correos |
| `tel:` | Teléfonos |

---

# Ejemplo práctico

```html
<a href="https://www.shimano.com">
    Visitar Shimano
</a>
```

---

# Ventajas de rutas absolutas

- Acceso global.
- Funcionan desde cualquier archivo.
- Ideales para recursos externos.

---

# Desventajas de rutas absolutas

- Dependencia del servidor externo.
- Si el recurso desaparece, el enlace falla.
- Requieren internet.

---

# Rutas Relativas

Las rutas relativas buscan recursos dentro del mismo proyecto.

Se basan en la ubicación del archivo actual.

---

# Ejemplo

```html
<a href="contacto.html">
    Contacto
</a>
```

---

# Características de las rutas relativas

- Dependen de la estructura del proyecto.
- Funcionan localmente.
- Son las más utilizadas en proyectos web.
- Facilitan mover proyectos completos.

---

# Ejemplo de estructura de proyecto

```txt
proyecto/
│
├── index.html
├── contacto.html
│
├── css/
│   └── estilos.css
│
├── js/
│   └── app.js
│
└── img/
    └── logo.png
```

---

# Archivo en la misma carpeta

```html
<a href="contacto.html">
```

HTML busca el archivo junto al documento actual.

---

# Acceder a una carpeta

```html
<img src="img/logo.png">
```

HTML entra a la carpeta `img`.

---

# Explicación visual

```txt
img/logo.png
│
├── img/
└── logo.png
```

---

# Subir una carpeta `../`

`../` significa:

```txt
Subir un nivel
```

---

# Ejemplo

```html
<img src="../logo.png">
```

---

# Ejemplo visual

```txt
proyecto/
│
├── logo.png
│
└── paginas/
    └── contacto.html
```

Si `contacto.html` quiere acceder a `logo.png`:

```html
<img src="../logo.png">
```

---

# Subir varios niveles

```html
../../archivo.html
```

Cada `../` sube una carpeta.

---

# Ejemplo visual

```txt
proyecto/
│
├── index.html
│
└── paginas/
    └── usuarios/
        └── perfil.html
```

Para volver a `index.html`:

```html
<a href="../../index.html">
```

---

# Ruta actual `./`

`./` significa:

```txt
Carpeta actual
```

---

# Ejemplo

```html
<img src="./logo.png">
```

Generalmente puede omitirse.

---

# Diferencia entre rutas

| Ruta | Tipo |
|---|---|
| `https://google.com` | Absoluta |
| `img/logo.png` | Relativa |
| `../logo.png` | Relativa |
| `./logo.png` | Relativa |

---

# Ejemplo completo

## HTML principal

```html
<h1>Rutas</h1>

<a href="paginas/contacto.html">
    Ir a contacto
</a>

<img src="img/logo.png" alt="Logo">
```

---

# Ejemplo de navegación

## Archivo actual

```txt
index.html
```

## Ruta

```html
<a href="servicios.html">
```

Resultado:

HTML busca:

```txt
/index.html
/servicios.html
```

---

# Error común

Incorrecto:

```html
<img src="/logo.png">
```

Sin comprender la raíz del proyecto.

---

# ¿Por qué ocurre?

La `/` inicial cambia el comportamiento hacia la raíz del servidor.

Esto puede romper rutas en proyectos locales.

---

# Correcto para proyectos básicos

```html
<img src="img/logo.png">
```

---

# Diferencia entre local y servidor

## Local

```txt
C:/proyecto/index.html
```

## Servidor

```txt
https://pagina.com/index.html
```

Las rutas relativas funcionan diferente dependiendo del entorno.

---

# Buenas prácticas

- Organizar recursos en carpetas.
- Utilizar nombres claros.
- Evitar espacios en nombres.
- Utilizar minúsculas.
- Mantener rutas limpias.

---

# Organización recomendada

```txt
proyecto/
│
├── index.html
│
├── css/
├── js/
├── img/
└── pages/
```

---

# Error común con mayúsculas

Incorrecto:

```html
<img src="Logo.png">
```

Si el archivo real es:

```txt
logo.png
```

En servidores Linux esto generará error.

---

# Recomendación

Utilizar siempre:

- Minúsculas
- Guiones
- Nombres simples

Ejemplo:

```txt
logo-html.png
```

---

# Rutas en CSS

CSS también utiliza rutas.

---

# Ejemplo

```css
background-image: url("../img/fondo.jpg");
```

---

# Rutas en JavaScript

JavaScript también trabaja con rutas.

---

# Ejemplo

```html
<script src="js/app.js"></script>
```

---

# Importancia de comprender rutas

Comprender rutas es fundamental para:

- Navegación web
- Carga de imágenes
- CSS
- JavaScript
- Frameworks
- Backend

---

# Analogía simple

Las rutas funcionan como direcciones de una casa.

Ejemplo:

```txt
Ciudad → Barrio → Calle → Casa
```

En HTML:

```txt
Proyecto → Carpeta → Archivo
```

---

# Resumen rápido

| Símbolo | Función |
|---|---|
| `./` | Carpeta actual |
| `../` | Subir carpeta |
| `/` | Raíz del servidor |

---

# Resumen de rutas

| Tipo | Ejemplo |
|---|---|
| Absoluta | `https://google.com` |
| Relativa | `img/logo.png` |
| Relativa subiendo nivel | `../logo.png` |

---

# Resumen de etiquetas

| Etiqueta | Función |
|---|---|
| `<a>` | Navegación |
| `<img>` | Mostrar imágenes |
| `<link>` | Cargar CSS |
| `<script>` | Cargar JavaScript |
