# Taller Básico de Excel
## Funciones, Análisis de Ventas y Diagrama de Pareto

---

# Objetivo del Taller

Aplicar los conocimientos vistos en clase sobre:

- Función `SI`
- Funciones anidadas
- Quitar duplicados
- Balance de ventas
- Promedios
- Análisis de datos
- Diagrama de Pareto

---

# Temas Trabajados

## Videos de referencia

1. Funciones Anidadas https://www.youtube.com/watch?v=1pu4D1Yna64 
2. Quitar Duplicados en Excel Básico https://www.youtube.com/watch?v=SQyCBTF7Urc&t=15s 
3. Función SI https://www.youtube.com/watch?v=EyVlVKOcHoA&t=269s  
4. Diagrama de Pareto https://www.youtube.com/watch?v=W5R43is-1AY&t=321s  

---

# Contexto del Taller

Una empresa desea analizar las ventas y egresos obtenidos durante un año.  
Usted deberá organizar la información en Excel y aplicar las funciones vistas en clase para generar reportes y análisis.

---

# Base de Datos

Digite la siguiente tabla en Excel.

| ID | Vendedor | Mes | Trimestre | Ventas | Egresos |
|---|---|---|---|---|---|
| 1 | Carlos | Enero | T1 | 2500 | 1200 |
| 2 | Ana | Febrero | T1 | 3200 | 1500 |
| 3 | Luis | Marzo | T1 | 2800 | 1300 |
| 4 | María | Abril | T2 | 4100 | 2000 |
| 5 | Pedro | Mayo | T2 | 3900 | 1800 |
| 6 | Laura | Junio | T2 | 4500 | 2100 |
| 7 | Carlos | Julio | T3 | 4700 | 2200 |
| 8 | Ana | Agosto | T3 | 5200 | 2500 |
| 9 | Luis | Septiembre | T3 | 4900 | 2300 |
| 10 | María | Octubre | T4 | 6100 | 2900 |
| 11 | Pedro | Noviembre | T4 | 5800 | 2700 |
| 12 | Laura | Diciembre | T4 | 6400 | 3000 |
| 13 | Carlos | Enero | T1 | 2500 | 1200 |
| 14 | Ana | Febrero | T1 | 3200 | 1500 |

---

# Parte 1 — Función SI

## Actividad

Crear una nueva columna llamada:

## Estado de Venta

Condiciones:

- Si la venta es mayor o igual a 5000 → `"Excelente"`
- Si la venta es mayor o igual a 4000 → `"Buena"`
- Si la venta es menor a 4000 → `"Regular"`

---

## Ejemplo esperado

| Ventas | Estado |
|---|---|
| 6200 | Excelente |
| 4500 | Buena |
| 2800 | Regular |

---

## Requisito

La solución debe realizarse utilizando:

- Función `SI`
- Funciones anidadas

---

# Parte 2 — Quitar Duplicados

## Actividad

La tabla contiene registros repetidos.

Debe:

1. Seleccionar toda la tabla.
2. Ir a:
   - Datos
   - Quitar duplicados
3. Eliminar los registros repetidos.

---

## Preguntas

1. ¿Cuántos registros quedaron después de quitar duplicados?
2. ¿Qué vendedores tenían datos repetidos?

---

# Parte 3 — Balance de Ventas

## Actividad

Realizar el balance de ventas de la empresa.

---

## 1. Balance Trimestral

Calcular las ventas totales por trimestre.

### Tabla sugerida

| Trimestre | Total Ventas |
|---|---|
| T1 | |
| T2 | |
| T3 | |
| T4 | |

---

## 2. Balance Semestral

### Primer semestre

Meses:

- Enero
- Febrero
- Marzo
- Abril
- Mayo
- Junio

### Segundo semestre

Meses:

- Julio
- Agosto
- Septiembre
- Octubre
- Noviembre
- Diciembre

---

## Tabla sugerida

| Semestre | Total Ventas |
|---|---|
| S1 | |
| S2 | |

---

## 3. Balance Anual

Calcular:

- Total de ventas del año
- Total de egresos del año

---

## Tabla sugerida

| Concepto | Valor |
|---|---|
| Total Ventas | |
| Total Egresos | |

---

# Parte 4 — Promedios

## Actividad

Calcular:

1. Promedio anual de ventas
2. Promedio anual de egresos

---

## Tabla sugerida

| Concepto | Promedio |
|---|---|
| Promedio Ventas | |
| Promedio Egresos | |

---

# Parte 5 — Análisis de Rendimiento

## Actividad

Crear una nueva columna llamada:

## Rendimiento

Condiciones:

- Si las ventas son mayores a 5500 → `"Alto"`
- Si las ventas están entre 4000 y 5499 → `"Medio"`
- Si las ventas son menores a 4000 → `"Bajo"`

---

# Parte 6 — Diagrama de Pareto

## Actividad

Con base en las ventas de cada vendedor:

1. Crear una tabla resumen.
2. Ordenar las ventas de mayor a menor.
3. Calcular:
   - Frecuencia acumulada
   - Porcentaje acumulado
4. Insertar:
   - Gráfico de columnas
   - Línea acumulada
5. Construir el diagrama de Pareto.

---

## Tabla sugerida

| Vendedor | Total Ventas | % Acumulado |
|---|---|---|
| | | |

---

# Preguntas de Análisis

1. ¿Qué trimestre tuvo mayores ventas?
2. ¿Qué semestre obtuvo más ingresos?
3. ¿Cuál vendedor generó más ventas?
4. ¿Qué porcentaje de vendedores genera la mayor parte de las ventas?
5. ¿Qué utilidad obtiene la empresa?
   - Fórmula:
   - Utilidad = Ventas - Egresos

---

# Requisitos Técnicos

El archivo debe contener:

- Hoja con la base de datos
- Hoja de balances
- Hoja de promedios
- Hoja del diagrama de Pareto

---

# Entregables

El estudiante debe entregar:

- Archivo Excel (.xlsx)

---

# Criterios de Evaluación

| Criterio | Valor |
|---|---|
| Uso correcto de función SI | 20% |
| Uso de funciones anidadas | 20% |
| Eliminación de duplicados | 15% |
| Balance trimestral, semestral y anual | 20% |
| Cálculo de promedios | 10% |
| Elaboración del Pareto | 15% |

---

# Recomendaciones

- Utilizar formato de tabla.
- Aplicar bordes y colores.
- Verificar que las fórmulas funcionen correctamente.
- Guardar constantemente el archivo.

```