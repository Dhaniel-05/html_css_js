# Enlaces o Anclas en HTML

Los enlaces permiten navegar entre:

- Páginas web
- Archivos
- Secciones internas
- Recursos externos
- Sitios web

Los enlaces son uno de los elementos más importantes de la web.

Sin enlaces, la navegación entre páginas no existiría.

---

# La etiqueta `<a>`

La etiqueta `<a>` significa:

```txt
Anchor
```

Traducido comúnmente como:

- Ancla
- Enlace
- Hipervínculo

---

# Estructura básica

```html
<a href="https://google.com">
    Google
</a>
```

---

# Explicación

| Parte | Función |
|---|---|
| `<a>` | Crea el enlace |
| `href` | Define el destino |
| `Google` | Texto visible |

---

# ¿Qué es `href`?

`href` significa:

```txt
Hyper Reference
```

Es la referencia o dirección del recurso al que apunta el enlace.

```html
<a href="https://google.com">
```

Sin `href`, el enlace pierde su funcionalidad.

---

# Texto visible del enlace

El contenido dentro de `<a>` es lo que el usuario verá en pantalla.

```html
<a href="https://google.com">
    Ir a Google
</a>
```

Resultado:

Ir a Google

---

# Ejemplo de enlaces externos

```html
<a href="https://www.google.com">
    Google
</a>

<a href="https://www.youtube.com">
    YouTube
</a>

<a href="https://www.facebook.com">
    Facebook
</a>
```

---

# Atributo `title`

Proporciona información adicional sobre el enlace.

El navegador normalmente muestra este texto cuando el usuario pasa el mouse sobre el enlace.

```html
<a href="https://youtube.com" title="Ir a YouTube">
    YouTube
</a>
```

---

# Importancia del atributo `title`

Tecnologías de asistencia como lectores de pantalla pueden utilizar este atributo para proporcionar contexto adicional al usuario.

Ayuda en:

- Accesibilidad
- Usabilidad
- Experiencia de usuario

---

# Enlaces internos

Permiten navegar entre archivos del mismo proyecto.

---

# Ejemplo

```html
<a href="pagina1.html">
    Ir a página 1
</a>
```

---

# Ejemplo práctico

## Archivo principal

```html
<a href="pagina1.html">
    Página 1
</a>

<a href="pagina2.html">
    Página 2
</a>
```

---

## Archivo `pagina1.html`

```html
<h1>Página 1</h1>

<a href="index.html">
    Volver al inicio
</a>
```

---

# Rutas relativas

Las rutas relativas buscan archivos dentro del proyecto actual.

```html
<a href="contacto.html">
```

---

# Rutas absolutas

Las rutas absolutas incluyen toda la dirección web.

```html
<a href="https://www.google.com">
```

---

# Error común

Incorrecto:

```html
<a>Google</a>
```

Correcto:

```html
<a href="https://google.com">
    Google
</a>
```

Sin `href` el enlace NO navega.

---

# Abrir enlaces en otra pestaña

Se utiliza el atributo:

```html
target="_blank"
```

---

# Ejemplo

```html
<a href="https://google.com" target="_blank">
    Google
</a>
```

---

# Explicación de `target`

| Valor | Función |
|---|---|
| `_self` | Abre en la misma pestaña |
| `_blank` | Abre en nueva pestaña |

---

# Comportamiento por defecto

Por defecto, todos los enlaces utilizan:

```html
target="_self"
```

Es decir:

- El enlace se abre en la misma pestaña.

---

# Buena práctica con `_blank`

Cuando se utiliza `target="_blank"` normalmente se recomienda agregar:

```html
rel="noopener noreferrer"
```

---

# Ejemplo completo

```html
<a 
    href="https://google.com"
    target="_blank"
    rel="noopener noreferrer"
>
    Google
</a>
```

---

# ¿Por qué usar `rel="noopener noreferrer"`?

Ayuda a mejorar:

- Seguridad
- Rendimiento
- Protección contra accesos no deseados entre pestañas

---

# Mala práctica: protocolo relativo

Incorrecto:

```html
<a href="//youtube.com">
```

Esto depende automáticamente del protocolo actual (`http` o `https`).

Actualmente es mejor especificar directamente:

```html
https://youtube.com
```

---

# Enlaces a secciones internas

Los enlaces también pueden navegar dentro de la misma página.

---

# Ejemplo

```html
<a href="#contacto">
    Ir a contacto
</a>
```

---

## Sección destino

```html
<h2 id="contacto">
    Contacto
</h2>
```

---

# Explicación

| Elemento | Función |
|---|---|
| `href="#contacto"` | Busca un id llamado contacto |
| `id="contacto"` | Punto de destino |

---

# Enlaces de correo

Permiten abrir aplicaciones de correo electrónico.

```html
<a href="mailto:correo@gmail.com">
    Enviar correo
</a>
```

---

# Enlaces telefónicos

Muy utilizados en dispositivos móviles.

```html
<a href="tel:+573001234567">
    Llamar
</a>
```

---

# Descargar archivos

El atributo `download` permite descargar archivos.

```html
<a href="archivo.pdf" download>
    Descargar PDF
</a>
```

---

# Enlaces como navegación

Los enlaces suelen utilizarse en:

- Menús
- Barras de navegación
- Sidebars
- Footers

---

# Ejemplo de menú

```html
<ul>
    <li><a href="index.html">Inicio</a></li>
    <li><a href="servicios.html">Servicios</a></li>
    <li><a href="contacto.html">Contacto</a></li>
</ul>
```

---

# Accesibilidad en enlaces

Buenas prácticas:

- Utilizar textos descriptivos.
- Evitar textos como:
  - "Click aquí"
  - "Más"
  - "Entrar"

---

# Incorrecto

```html
<a href="contacto.html">
    Click aquí
</a>
```

---

# Correcto

```html
<a href="contacto.html">
    Ir a la página de contacto
</a>
```

---

# ¿Por qué es importante?

Los lectores de pantalla leen los enlaces.

Si el texto no describe correctamente el destino, la navegación accesible se vuelve difícil.

---

# Diferencia entre HTML y CSS

HTML define:

- El destino
- La estructura
- La navegación

CSS define:

- Colores
- Tamaños
- Hover
- Apariencia visual

---

# Ejemplo HTML

```html
<a href="https://google.com">
    Google
</a>
```

---

# Ejemplo CSS

```css
a {
    color: blue;
    text-decoration: none;
}
```

---

# Emmet para enlaces

## Crear enlace rápido

```txt
a
```

Genera:

```html
<a href=""></a>
```

---

# Estructura semántica recomendada

```html
<nav>
    <a href="index.html">Inicio</a>
    <a href="servicios.html">Servicios</a>
    <a href="contacto.html">Contacto</a>
</nav>
```

---

# Buenas prácticas generales

- Utilizar textos claros.
- Verificar rutas correctamente.
- Utilizar `https`.
- Usar `target="_blank"` solo cuando sea necesario.
- Mantener navegación organizada.
- Evitar enlaces rotos.

---

# Resumen rápido

| Elemento | Función |
|---|---|
| `<a>` | Crear enlace |
| `href` | Destino del enlace |
| `title` | Información adicional |
| `target` | Define dónde abrir |
| `_blank` | Nueva pestaña |
| `_self` | Misma pestaña |
| `download` | Descargar archivo |
| `mailto:` | Abrir correo |
| `tel:` | Realizar llamada |
| `id` | Punto de navegación interna |
