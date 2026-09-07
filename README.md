# Automated Data Audit & Conciliation Pipeline 📊🚀

Este repositorio contiene un ecosistema de scripts en Python desarrollado en entornos Jupyter/Colab para resolver uno de los problemas operativos más críticos en las empresas: la conciliación automatizada de datos y la auditoría estricta de reportes masivos de Excel que presentan inconsistencias de captura manual.

## 🛠️ Tecnologías y Conceptos Clave
* **Python 3.x**
* **Pandas:** Uso avanzado de `DataFrames`, uniones estructurales (`outer merges`), tratamiento de tipos de datos y indexación dinámica.
* **Regex (Expresiones Regulares):** Tratamiento y homologación de patrones de texto complejos (razones sociales, siglas viales).
* **Unicodedata:** Estandarización de caracteres Unicode, eliminación de acentos y manejo de espacios especiales (`NBSP`, `NFD`).
* **Glob & OS:** Escaneo automatizado de directorios locales para procesar múltiples informes operativos simultáneamente.

## ✨ Arquitectura del Proyecto (Módulos)

### 1️⃣ Canalización de Limpieza y Homologación de Datos
* **Normalización Avanzada:** Corrige errores clásicos de formateo (como códigos postales o IDs numéricos transformados erróneamente en flotantes de texto `20210.0` ➡️ `20210`).
* **Algoritmo Corporativo Inteligente:** Normaliza e iguala registros dispares de razones sociales (`S.A. DE C.V.` vs `sa de cv`) y abreviaturas de vialidades (`Blvd.`, `Av.`, `Carr.`) para evitar falsos negativos en los cruces.
* **Ingesta Dinámica:** Escanea las primeras filas de los archivos Excel para localizar de forma automática el encabezado real mediante la coincidencia de columnas clave.

### 2️⃣ Motor de Auditoría Estricta y Conciliación
* Ejecuta un **Outer Join matricial** completo para confrontar una base de datos maestra (Testigo) contra múltiples archivos satélite de forma masiva.
* Segmenta y exporta dinámicamente un reporte maestro final en Excel estructurado en pestañas automatizadas según el tipo de discrepancia:
  * ❌ **Folios Faltantes:** Registros omitidos en la operación.
  * 💰 **Diferencia Costos:** Descuadres financieros redondeados matemáticamente a dos decimales.
  * 📍 **Diferencia Dirección y CP:** Errores de ubicación y códigos postales extraídos.

## 🚀 Impacto en el Negocio
* **Mitigación de Riesgos Financieros:** Identifica instantáneamente desviaciones de costos y errores de facturación.
* **Automatización de Auditorías:** Transforma un proceso manual que toma días de validación por equipos de finanzas y operaciones, en una ejecución precisa de solo unos segundos.
