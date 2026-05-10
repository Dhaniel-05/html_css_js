# Formularios en HTML

La etiqueta `<form>` se utiliza para crear formularios.

Un formulario permite capturar información del usuario y enviarla a un servidor.

---

# Atributos importantes del formulario

## `action`

Define la URL o archivo donde se enviarán los datos del formulario.

```html
<form action="/registro">
```

---

## `method`

Define cómo se enviarán los datos.

HTML oficialmente soporta solo dos métodos:

- `GET`
- `POST`

---

# Método GET

Envía los datos por la URL.

Ejemplo:

```txt
https://pagina.com?nombre=Daniel&edad=25
```

## Características

- Los datos son visibles en la URL.
- Tiene límite de caracteres.
- Puede guardarse en historial y favoritos.
- Se utiliza normalmente en:
  - Búsquedas
  - Filtros
  - Formularios simples

## Ejemplo

```html
<form action="/buscar" method="get">
```

---

# Método POST

Envía los datos internamente dentro de la petición HTTP.

Los datos NO aparecen en la URL.

## Características

- Más seguro que GET.
- Permite enviar grandes cantidades de datos.
- Permite subir archivos.
- Se utiliza normalmente en:
  - Inicios de sesión
  - Registros
  - Formularios sensibles
  - Envío de archivos

## Ejemplo

```html
<form action="/registro" method="post">
```

---

# ¿Existen otros métodos?

A nivel del protocolo HTTP sí existen otros métodos como:

- `PUT`
- `PATCH`
- `DELETE`

Pero los formularios HTML tradicionales NO los soportan directamente.

Estos métodos normalmente se utilizan mediante:

- JavaScript (`fetch` o `axios`)
- APIs REST
- Frameworks backend

---

# Equivalencias GET y POST

| Método | Visible en URL | Más seguro | Uso común |
|---|---|---|---|
| GET | Sí | No | Búsquedas |
| POST | No | Sí | Registros e inicio de sesión |

---

# Estructura básica de un formulario

```html
<form action="" method="post">

</form>
```

---

# La etiqueta `<input>`

La etiqueta `<input>` permite capturar datos del usuario.

```html
<input type="text">
```

---

# Atributos importantes de los inputs

---

## `type`

Define el tipo de campo.

Ejemplos:

```html
type="text"
type="email"
type="password"
type="checkbox"
type="radio"
type="file"
type="date"
```

---

## `name`

Es el nombre interno del campo.

El servidor utiliza este nombre para identificar la información enviada.

```html
<input name="correo">
```

Este atributo NO es visible para el usuario.

---

## `id`

Es un identificador único.

Se utiliza para:

- Relacionar labels
- Aplicar estilos CSS
- Manipular elementos con JavaScript

```html
<input id="correo">
```

---

## `placeholder`

Muestra un texto de ayuda dentro del input.

```html
<input placeholder="Ingrese su correo">
```

---

## `required`

Hace obligatorio el campo.

```html
<input required>
```

---

## `readonly`

Hace que el campo sea solo lectura.

El usuario no puede modificarlo.

```html
<input readonly>
```

---

## `disabled`

Desactiva completamente el campo.

El usuario NO puede interactuar con él y el valor NO se envía al servidor.

```html
<input disabled>
```

---

# Diferencia entre `readonly` y `disabled`

## `readonly`

- El usuario NO puede modificar el contenido.
- El valor SÍ se envía al servidor.

```html
<input readonly value="Daniel">
```

---

## `disabled`

- El usuario NO puede interactuar con el campo.
- El valor NO se envía al servidor.

```html
<input disabled value="Daniel">
```

---

## `value`

Define un valor inicial.

```html
<input value="Daniel">
```

---

# Tipos de input

---

# `type="text"`

Campo de texto básico.

```html
<input type="text">
```

---

# `type="email"`

Permite ingresar correos electrónicos.

El navegador valida automáticamente el formato.

```html
<input type="email">
```

---

# `type="password"`

Oculta los caracteres ingresados.

```html
<input type="password">
```

---

# `type="checkbox"`

Permite seleccionar varias opciones.

```html
<input type="checkbox">
```

---

# `type="radio"`

Permite seleccionar UNA sola opción.

```html
<input type="radio">
```

## Importante

Los radio buttons deben compartir el mismo `name`.

```html
<input type="radio" name="genero">
<input type="radio" name="genero">
```

---

# `type="file"`

Permite subir archivos.

```html
<input type="file">
```

---

# `type="date"`

Permite seleccionar fechas.

```html
<input type="date">
```

---

# `<textarea>`

Permite ingresar texto largo.

```html
<textarea></textarea>
```

## Se utiliza normalmente para:

- Comentarios
- Descripciones
- Mensajes
- Observaciones

---

# `<select>` y `<option>`

Permiten crear listas desplegables.

```html
<select>
    <option>Colombia</option>
    <option>México</option>
    <option>Argentina</option>
</select>
```

---

# La etiqueta `<label>`

La etiqueta `<label>` sirve para asociar texto descriptivo a un input.

---

# Forma 1: usando `for` e `id`

La forma más recomendada.

```html
<label for="correo">Correo:</label>

<input type="email" id="correo">
```

## Ventajas

- Mejor accesibilidad
- Más organizado
- Más profesional
- Facilita mantenimiento

---

# Forma 2: encerrando el input dentro del label

```html
<label>
    Correo:
    <input type="email">
</label>
```

También funciona correctamente.

---

# ¿Cuál es la mejor práctica?

La forma más recomendada es:

```html
label + for + id
```

Porque mejora:

- Accesibilidad
- Organización
- Compatibilidad
- Mantenimiento del código

---

# Botones en formularios

La etiqueta `<button>` permite crear botones.

---

## `type="submit"`

Envía toda la información del formulario.

```html
<button type="submit">
    Enviar formulario
</button>
```

---

## `type="button"`

Crea un botón normal.

No envía el formulario automáticamente.

```html
<button type="button">
    Click
</button>
```

---

## `type="reset"`

Restablece los campos del formulario.

```html
<button type="reset">
    Limpiar formulario
</button>
```

---

# Resumen

| Elemento | Función |
|---|---|
| `<form>` | Crear formularios |
| `<input>` | Capturar datos |
| `<textarea>` | Texto largo |
| `<select>` | Lista desplegable |
| `<option>` | Opción de lista |
| `<label>` | Describir inputs |
| `type` | Tipo de campo |
| `name` | Nombre interno |
| `id` | Identificador único |
| `placeholder` | Texto de ayuda |
| `required` | Campo obligatorio |
| `readonly` | Solo lectura |
| `disabled` | Campo desactivado |
| `value` | Valor inicial |
| `button` | Crear botones |

```