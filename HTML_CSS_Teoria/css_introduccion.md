# Introducción a CSS

CSS significa:

```txt
Cascading Style Sheets
```

Traducido:

```txt
Hojas de Estilo en Cascada
```

CSS es el lenguaje encargado de definir la apariencia visual de una página web.

Mientras HTML estructura el contenido, CSS se encarga de:

- Colores
- Tamaños
- Espaciados
- Posiciones
- Fuentes
- Diseño visual
- Responsive Design
- Animaciones

---

# Relación entre HTML y CSS

HTML define:

```txt
Qué existe
```

CSS define:

```txt
Cómo se ve
```

---

# Analogía simple

## HTML

Es la estructura de una casa:

- Paredes
- Puertas
- Ventanas

---

## CSS

Es la apariencia visual:

- Pintura
- Decoración
- Iluminación
- Distribución visual

---

# CSS NO existe sin HTML

CSS necesita elementos HTML para aplicar estilos.

Por esa razón normalmente primero se construye:

1. HTML
2. Luego CSS

---

# ¿Qué significa "en cascada"?

La palabra:

```txt
Cascade
```

significa:

```txt
Cascada
```

---

# ¿Por qué "cascada"?

Porque múltiples estilos pueden aplicarse al mismo elemento.

CSS decide cuál estilo tiene mayor prioridad.

---

# Analogía de la cascada

Imagina agua cayendo desde distintos niveles.

El agua que viene desde más arriba tiene mayor fuerza y domina el flujo inferior.

En CSS ocurre algo parecido:

- Algunos estilos tienen más prioridad.
- Algunos pueden sobrescribir otros estilos.

---

# Ejemplo conceptual

```css
p {
    color: blue;
}

p {
    color: red;
}
```

Resultado:

```txt
El texto será rojo
```

Porque el último estilo sobrescribe el anterior.

---

# Importancia de entender la cascada

Cuando una página crece, múltiples estilos pueden afectar un mismo elemento.

CSS analiza:

- Orden
- Prioridad
- Especificidad
- Herencia

Para decidir qué estilo aplicar.

---

# CSS no se trata solo de cambiar colores

Muchos principiantes creen que CSS consiste únicamente en modificar propiedades visuales.

Pero CSS realmente trata de:

- Relaciones entre elementos
- Distribución
- Flujo visual
- Jerarquías
- Comportamientos visuales

---

# Relación entre elementos

CSS trabaja constantemente con relaciones como:

| Relación | Ejemplo |
|---|---|
| Padre | Contenedor principal |
| Hijo | Elemento dentro del padre |
| Hermano | Elementos al mismo nivel |
| Nieto | Hijo de un hijo |

---

# Ejemplo visual

```html
<section>
    <div>
        <p>Texto</p>
    </div>
</section>
```

---

# Jerarquía

```txt
section → Padre
div → Hijo
p → Nieto
```

---

# HTML usa atributos, CSS usa propiedades

Es importante NO confundir:

- Atributos HTML
- Propiedades CSS

---

# Atributos HTML

Los atributos agregan configuración o comportamiento.

```html
<input type="text">
```

Aquí:

```txt
type
```

es un atributo HTML.

---

# Propiedades CSS

Las propiedades CSS modifican la apariencia visual.

```css
color: blue;
```

Aquí:

```txt
color
```

es una propiedad CSS.

---

# Diferencia importante

| HTML | CSS |
|---|---|
| Atributos | Propiedades |
| Estructura | Apariencia |
| Configuración | Estilos |

---

# Sintaxis básica de CSS

```css
selector {
    propiedad: valor;
}
```

---

# Ejemplo

```css
p {
    color: blue;
    font-size: 20px;
}
```

---

# Explicación

| Parte | Función |
|---|---|
| `p` | Selector |
| `color` | Propiedad |
| `blue` | Valor |

---

# ¿Qué es un selector?

El selector indica:

```txt
Qué elemento será modificado
```

---

# Ejemplo

```css
h1 {
    color: red;
}
```

Todos los `h1` serán rojos.

---

# Formas de enlazar CSS

Existen 3 formas principales de utilizar CSS.

---

# 1. CSS Inline

Se escribe directamente dentro del HTML utilizando el atributo `style`.

---

# Ejemplo

```html
<p style="color: blue;">
    Texto azul
</p>
```

---

# ¿Por qué se llama inline?

Porque el estilo se escribe:

```txt
En la misma línea del HTML
```

---

# Desventajas del CSS inline

## Mala práctica 1

Mezcla:

- HTML
- CSS

en el mismo lugar.

---

## Mala práctica 2

Dificulta:

- Lectura
- Mantenimiento
- Escalabilidad

---

# Problema real

Cuando un proyecto crece:

- El código se vuelve difícil de mantener.
- Encontrar errores es más complicado.
- Reutilizar estilos es difícil.

---

# Además

Los estilos inline tienen mucha prioridad.

Sobrescribirlos luego puede ser problemático.

Muchas veces obliga al uso de:

```css
!important
```

---

# ¿Por qué `!important` es mala práctica?

Porque rompe parcialmente la lógica natural de la cascada.

Genera:

- Código difícil de mantener
- Confusión
- Problemas de escalabilidad

---

# 2. CSS Interno

Se utiliza la etiqueta `<style>` dentro del HTML.

---

# Ejemplo

```html
<style>
    h1 {
        color: blue;
    }
</style>
```

---

# Ventajas

- Más organizado que inline.
- Permite escribir múltiples estilos.

---

# Desventajas

- Sigue mezclando HTML y CSS.
- No es reutilizable entre páginas.
- Dificulta proyectos grandes.

---

# 3. CSS Externo

Es la forma recomendada profesionalmente.

CSS se escribe en archivos separados.

---

# Ejemplo HTML

```html
<link rel="stylesheet" href="styles.css">
```

---

# Archivo CSS

```css
h1 {
    color: blue;
}
```

---

# Ventajas del CSS externo

- Código más limpio.
- Mejor organización.
- Reutilizable.
- Fácil mantenimiento.
- Escalable.
- Más profesional.

---

# La etiqueta `<link>`

Permite conectar archivos externos.

---

# Ejemplo

```html
<link rel="stylesheet" href="styles.css">
```

---

# Explicación

| Parte | Función |
|---|---|
| `link` | Vincular recurso |
| `rel` | Relación del archivo |
| `stylesheet` | Hoja de estilos |
| `href` | Ruta del archivo |

---

# ¿Qué significa `rel`?

`rel` significa:

```txt
Relationship
```

Indica la relación entre el documento HTML y el archivo enlazado.

---

# ¿Qué significa `href`?

Define la ubicación del archivo CSS.

```html
href="styles.css"
```

---

# Ejemplo completo

## HTML

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">

    <title>CSS</title>

    <link rel="stylesheet" href="styles.css">
</head>

<body>

    <h1>Título</h1>

    <p>
        Texto de ejemplo
    </p>

</body>
</html>
```

---

# Archivo `styles.css`

```css
h1 {
    color: #333;
    font-size: 40px;
}

p {
    color: #666;
    font-size: 20px;
}
```

---

# Reset CSS básico

Muchos navegadores agregan estilos automáticamente.

Por eso suele utilizarse:

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```

---

# ¿Qué hace el selector `*`?

Selecciona:

```txt
Todos los elementos
```

---

# Explicación

| Propiedad | Función |
|---|---|
| `margin: 0` | Elimina márgenes |
| `padding: 0` | Elimina rellenos |
| `box-sizing: border-box` | Mejora cálculo de tamaños |

---

# Cascada y prioridad

CSS tiene un sistema de prioridades.

---

# Prioridad simplificada

| Tipo | Prioridad |
|---|---|
| Inline | Muy alta |
| Interno | Media |
| Externo | Normal |

---

# Pero también influye

- Especificidad
- Orden
- Herencia
- `!important`

---

# Herencia en CSS

Algunas propiedades se heredan automáticamente.

Ejemplo:

```css
body {
    color: blue;
}
```

Los textos internos normalmente heredarán ese color.

---

# CSS moderno

Hoy CSS permite construir:

- Layouts completos
- Animaciones
- Responsive Design
- Interfaces modernas
- Sistemas visuales complejos

---

# CSS no trabaja elemento por elemento

CSS realmente funciona como:

```txt
Un sistema de relaciones visuales
```

No se trata únicamente de:

```txt
Modificar cajas individualmente
```

Sino entender:

- Cómo interactúan
- Cómo se distribuyen
- Cómo se posicionan
- Cómo responden entre sí

---

# Buenas prácticas

- Utilizar CSS externo.
- Mantener HTML limpio.
- Evitar `!important`.
- Utilizar nombres claros.
- Organizar propiedades.
- Comprender la cascada antes de memorizar estilos.

---

# Resumen 

| Concepto | Función |
|---|---|
| HTML | Estructura |
| CSS | Apariencia |
| Selector | Elemento a modificar |
| Propiedad | Característica visual |
| Valor | Configuración aplicada |
| Cascada | Sistema de prioridades |

---

# Formas de usar CSS

| Forma | Recomendación |
|---|---|
| Inline | No recomendada |
| Interno | Poco recomendada |
| Externo | Recomendado |

---

# Resumen de etiquetas

| Etiqueta | Función |
|---|---|
| `<style>` | CSS interno |
| `<link>` | Conectar CSS externo |
