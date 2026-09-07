# Data Cleansing & Text Normalization Pipeline 📊🚀

Este proyecto resuelve uno de los mayores problemas operativos en el análisis de datos corporativos: la inconsistencia en los registros manuales de texto (direcciones, razones sociales, códigos postales y datos numéricos mal formateados). 

Desarrollé un pipeline automatizado en Python capaz de estandarizar bases de datos complejas para auditorías, cruces de información o procesos de ETL (Extract, Transform, Load), minimizando los falsos negativos al comparar registros.

## 🛠️ Tecnologías y Conceptos Utilizados
* **Python 3.x**
* **Pandas:** Carga dinámica y manipulación estructural de DataFrames de gran volumen.
* **Regex (Expresiones Regulares):** Tratamiento avanzado de texto, detección de abreviaturas y mapeo de patrones complejos.
* **Unicodedata:** Normalización de caracteres Unicode (remoción de acentos y gestión de espacios ocultos o especiales).

## ✨ Características Principales del Código
1. **Normalización Inteligente:** Convierte texto eliminando acentos, estandariza espacios especiales (`NBSP`, `NFD`) y soluciona el típico error de flotantes convertidos a texto por Excel (`20210.0` ➡️ `20210`).
2. **Algoritmo de Homologación Corporativa:** Convierte e iguala diferentes escrituras de razones sociales (`S.A. DE C.V.`, `sa de cv`, `S. A.`) y abreviaturas viales (`Blvd.`, `Carr.`, `Col.`) a un formato único comparable sin alterar el archivo original.
3. **Ingesta de Datos Dinámica:** Lee archivos de Excel localizando de forma automática la fila exacta donde inician los encabezados reales mediante un sistema inteligente de coincidencia de columnas clave (`id ine`, `empresa`, etc.).

## 🚀 Impacto en el Negocio
* **Ahorro de Tiempo:** Reduce en un 90% las horas invertidas manualmente por los equipos de operaciones y finanzas en la conciliación de reportes.
* **Integridad de Datos:** Asegura auditorías precisas al evitar duplicados ocultos por errores ortográficos o de captura de datos.
