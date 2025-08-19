# Análisis de Cancelación de Clientes - TelecomX LATAM

Este repositorio contiene el análisis exploratorio de datos (EDA) realizado para identificar los factores que influyen en la cancelación de servicios por parte de los clientes de TelecomX LATAM. El objetivo es proporcionar información clave al equipo de Data Science para el desarrollo de modelos predictivos y estrategias de retención.

## Contenido del Notebook

El notebook `TelecomX_LATAM.ipynb` incluye los siguientes pasos:

1.  **Extracción de Datos:**
    *   Carga de datos desde un archivo JSON alojado en GitHub.

2.  **Transformación de Datos:**
    *   Normalización de columnas anidadas (`customer`, `phone`, `internet`, `account`) en el DataFrame principal.
    *   Eliminación de las columnas anidadas originales.
    *   Renombrado de columnas a un formato más descriptivo y en español.
    *   Detección y tratamiento de valores ausentes y strings vacíos en las columnas 'cancelo' y 'gastos_totales'.
    *   Eliminación de filas con valores nulos en las columnas tratadas.
    *   Corrección de tipos de datos para un análisis adecuado (conversión a float, string, int y category).
    *   Verificación y eliminación de duplicados (si existieran).
    *   Creación de la columna 'cuentas_diarias' calculando el gasto diario a partir del gasto mensual.
    *   Estandarización y transformación de variables booleanas a tipo entero (0 o 1).

3.  **Carga y Análisis:**
    *   **Análisis Descriptivo:** Obtención de estadísticas descriptivas para las variables numéricas.
    *   **Recuento de Cancelación:** Cálculo del porcentaje de cancelación por diferentes variables categóricas y binarias (`genero`, `servicio_telefonico`, `lineas_multiples`, `servicio_internet`, `seguridad_en_linea`, `Soporte_en_linea`, `proteccion_dispositivos`, `soporte_tecnico`, `servicio_tv`, `servicio_peliculas`, `tipo_contrato`, `metodo_pago`, `mayor_de_65`, `tiene_pareja`, `tiene_dependentes`).
    *   **Distribución de Cancelación:** Visualización de la tasa de cancelación a través de gráficos de barras y boxplots para variables clave.

4.  **Informe Final:**
    *   **Introducción:** Descripción del objetivo del análisis.
    *   **Limpieza y Tratamiento de Datos:** Resumen del proceso de preparación de datos.
    *   **Análisis Exploratorio de Datos:** Presentación de los principales hallazgos del análisis, incluyendo el perfil del cliente que cancela y los factores más influyentes.
    *   **Recomendaciones Estratégicas:** Propuesta de acciones basadas en los hallazgos para reducir la tasa de cancelación (optimización del servicio, fomento de contratos a largo plazo, paquetes integrales, segmentación de ofertas, etc.).
    *   **Gráficos:** Visualización de los gráficos generados durante el análisis.

## Cómo ejecutar el Notebook

Para ejecutar este notebook, necesitarás tener instalado Python y las siguientes librerías:

*   pandas
*   numpy
*   seaborn
*   matplotlib
