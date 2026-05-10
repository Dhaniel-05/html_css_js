# Listas en HTML

Las listas en HTML permiten organizar información de manera estructurada.

Se utilizan para:

- Enumerar pasos
- Mostrar menús
- Agrupar elementos relacionados
- Crear navegación
- Mostrar características o ingredientes

---

# Tipos de listas en HTML

HTML posee principalmente dos tipos de listas:

| Tipo | Etiqueta |
|---|---|
| Lista ordenada | `<ol>` |
| Lista no ordenada | `<ul>` |

---

# La etiqueta `<li>`

La etiqueta `<li>` significa:

```txt
List Item
```

Se utiliza para representar cada elemento de una lista.

```html
<li>Elemento</li>
```

---

# Listas ordenadas `<ol>`

Las listas ordenadas se utilizan cuando los elementos tienen un orden específico.

Por ejemplo:

- Pasos de una receta
- Tutoriales
- Instrucciones
- Rankings
- Procedimientos

---

# Ejemplo básico

```html
<ol>
    <li>Primer elemento</li>
    <li>Segundo elemento</li>
    <li>Tercer elemento</li>
</ol>
```

Resultado:

1. Primer elemento  
2. Segundo elemento  
3. Tercer elemento  

---

# Ejemplo práctico

```html
<ol>
    <li>Lavar las frutas</li>
    <li>Agregar agua</li>
    <li>Agregar azúcar</li>
    <li>Licuar</li>
    <li>Servir</li>
</ol>
```

---

# Atributo `type`

Permite cambiar el tipo de numeración.

---

## Letras mayúsculas

```html
<ol type="A">
```

Resultado:

A. Primero  
B. Segundo  
C. Tercero  

---

## Letras minúsculas

```html
<ol type="a">
```

Resultado:

a. Primero  
b. Segundo  
c. Tercero  

---

## Números romanos mayúsculos

```html
<ol type="I">
```

Resultado:

I. Primero  
II. Segundo  
III. Tercero  

---

## Números romanos minúsculos

```html
<ol type="i">
```

Resultado:

i. Primero  
ii. Segundo  
iii. Tercero  

---

# Atributo `start`

Permite iniciar la lista desde otro número.

```html
<ol start="5">
    <li>Cinco</li>
    <li>Seis</li>
    <li>Siete</li>
</ol>
```

Resultado:

5. Cinco  
6. Seis  
7. Siete  

---

# Atributo `reversed`

Invierte el orden de la numeración.

```html
<ol start="5" reversed>
    <li>Cinco</li>
    <li>Cuatro</li>
    <li>Tres</li>
</ol>
```

Resultado:

5. Cinco  
4. Cuatro  
3. Tres  

---

# Listas no ordenadas `<ul>`

Las listas no ordenadas se utilizan cuando el orden NO es importante.

Por ejemplo:

- Ingredientes
- Características
- Menús
- Categorías

---

# Ejemplo básico

```html
<ul>
    <li>Frutas</li>
    <li>Agua</li>
    <li>Azúcar</li>
</ul>
```

Resultado:

- Frutas
- Agua
- Azúcar

---

# Ejemplo práctico

```html
<ul>
    <li>Inicio</li>
    <li>Acerca de</li>
    <li>Servicios</li>
    <li>Contacto</li>
</ul>
```

Este tipo de lista suele utilizarse en menús de navegación.

---

# Diferencia entre `<ol>` y `<ul>`

| Etiqueta | Uso |
|---|---|
| `<ol>` | Cuando el orden importa |
| `<ul>` | Cuando el orden no importa |

---

# Buenas prácticas

- Utilizar `<ol>` para procesos o pasos.
- Utilizar `<ul>` para agrupaciones generales.
- Mantener listas organizadas y legibles.
- Utilizar `<li>` para cada elemento.

---

# Error común

Incorrecto:

```html
<ol>
    Texto
</ol>
```

Correcto:

```html
<ol>
    <li>Texto</li>
</ol>
```

Las listas deben contener elementos `<li>`.

---

# Anidación de listas

Las listas pueden contener otras listas.

```html
<ul>
    <li>
        Frutas
        <ul>
            <li>Manzana</li>
            <li>Pera</li>
        </ul>
    </li>
</ul>
```

---

# Ejemplo de estructura anidada

Resultado:

- Frutas
  - Manzana
  - Pera

---

# Emmet para listas

## Crear lista rápida

```txt
ul>li*3
```

Genera:

```html
<ul>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

---

# Accesibilidad y semántica

Las listas ayudan a:

- Organizar información
- Mejorar accesibilidad
- Facilitar lectura
- Mejorar estructura semántica

Los lectores de pantalla reconocen automáticamente las listas y ayudan a navegar el contenido correctamente.

---

# Resumen rápido

| Etiqueta | Función |
|---|---|
| `<ol>` | Lista ordenada |
| `<ul>` | Lista no ordenada |
| `<li>` | Elemento de lista |
| `type` | Cambia numeración |
| `start` | Cambia inicio |
| `reversed` | Invierte orden |
