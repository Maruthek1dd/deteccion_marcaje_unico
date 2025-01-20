# Detección de Marcajes Únicos de Empleados

Este proyecto tiene como objetivo procesar un conjunto de datos de marcajes de entrada y salida de empleados, y asegurar que cada empleado tenga solo un marcaje por día, tanto de entrada como de salida. Se realizan las siguientes tareas de procesamiento y análisis:

## Objetivo

1. **Filtrado de Datos**: Los datos provienen de un archivo de registro con múltiples columnas (fecha, hora, legajo, estado, etc.). Se separan en dos DataFrames distintos: uno para los marcajes de **entrada** y otro para los marcajes de **salida**.
   
2. **Marcaje Único**: Para cada legajo y fecha, se asegura que solo exista un marcaje de entrada y uno de salida por día. Si un legajo marca más de una vez el mismo día (por entrada o salida), se eliminan los registros duplicados.

3. **Detección de Inconsistencias**: Se identifican los legajos que tienen solo un marcaje de entrada o solo uno de salida, lo cual podría indicar un error en el registro de datos.

## Cómo Funciona

1. **Lectura de Datos**: Los datos se leen desde un archivo CSV o TXT, usando la biblioteca `pandas` para cargar y procesar la información.

2. **Separación por Estado**: Se divide el DataFrame en dos partes, una para los marcajes de entrada y otra para los de salida. Esto se logra filtrando los valores en la columna "estado".

3. **Eliminación de Duplicados**: Se eliminan las filas duplicadas por legajo y fecha, dejando solo una entrada y una salida por día.

4. **Detección de Inconsistencias**: Se agrupan los datos por legajo y fecha para verificar si cada legajo tiene solo una entrada y una salida al día.

5. **Generación del Archivo de Resultados**: Los resultados se guardan en un nuevo archivo CSV o TXT, que contiene los legajos con sus respectivas fechas y las marcas únicas de entrada y salida.

## Requisitos

- Python 3.x
- Pandas
- Matplotlib (si se generan gráficos)
- Jupyter Notebook (opcional para análisis interactivo)

## Instalación

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/deteccion_marcajes_unicos.git
