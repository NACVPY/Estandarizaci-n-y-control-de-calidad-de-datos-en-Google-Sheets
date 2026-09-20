# 🧹 Proyecto : Estandarización y Control de Calidad de Datos en Google Sheets

## 📌 Descripción del Proyecto
Este proyecto simula un escenario real de limpieza, normalización y validación de una base de datos de clientes desorganizada. El objetivo principal es transformar datos crudos (*raw data*) con múltiples inconsistencias de formato en una base de datos funcional, estructurada y lista para su análisis u uso operativo por parte de departamentos de Ventas o Marketing.

---

## 🛠️ Herramientas y Funciones Utilizadas
* **Herramienta:** Google Sheets
* **Estructura:** Arquitectura modular de dos pestañas (`01_Raw_Data` y `02_Clean_Data`).
* **Fórmulas y Funciones de Limpieza:**
  * `ESPACIOS` (`TRIM`) y `NOMPROPIO` (`PROPER`): Eliminación de espacios sobrantes y estandarización de nombres propios y ciudades.
  * `MINUSC` (`LOWER`) y `MAYUSC` (`UPPER`): Normalización de correos electrónicos y estados de cuenta.
  * `REGEXREPLACE` + `TEXTO`: Expresiones regulares para la extracción y limpieza profunda de caracteres no numéricos en números de teléfono.
* **Gobierno de Datos / Control de Entrada:**
  * **Reglas de Validación de Datos:** Implementación de menús desplegables para restringir valores (`ACTIVO`, `INACTIVO`, `PENDIENTE`) y verificación de sintaxis de correo electrónico.
  * **Deduplicación:** Eliminación de registros duplicados basados en claves primarias (`ID`).

---

## 📊 Flujo de Trabajo (Pipeline)

1. **Ingesta y Aislamiento:** Copia de seguridad de los datos originales en la pestaña `01_Raw_Data` para mantener la trazabilidad.
2. **Transformación:** Aplicación de fórmulas de limpieza en la pestaña `02_Clean_Data`.
3. **Consolidación:** Conversión de fórmulas a valores estáticos para congelar los datos procesados.
4. **Control de Calidad:** Aplicación de reglas de validación en la columna de correos y menús desplegables en campos críticos para evitar futuros errores de entrada manual.

---

## 🔗 Enlaces y Recursos
* **Hoja de Cálculo (Google Sheets):** https://docs.google.com/spreadsheets/d/1kxBN4s104RmpM8w5CSYNEeO12Ku-p5EM1yaLHcjt3fo/edit?usp=sharing
# Estandarización-y-control-de-calidad-de-datos-en-Google-Sheets
Este proyecto simula un escenario real de limpieza, normalización y validación de una base de datos de clientes desorganizada.
