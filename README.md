# Dashboard de Análisis de Ventas y Margen de Ganancia — Power BI

Este proyecto consiste en un dashboard interactivo desarrollado en **Power BI Desktop** para el análisis visual de KPIs de ventas, margen de ganancia (`Profit Margin %`) y rendimiento por categorías/regiones a partir del dataset `ventas_procesadas_pBI`.

---

## 📊 Descripción General

El objetivo de este proyecto es transformar datos de ventas en visualizaciones métricas de alto impacto para la toma de decisiones empresariales. Se abordó especialmente el formateo y cálculo preciso del **Margen de Ganancia Promedio**, resolviendo discrepancias de escala de porcentajes mediante expresiones dinámicas en **DAX**.

---

## 🛠️ Tecnologías y Herramientas Utilizadas

* **Power BI Desktop**: Diseño de tablero, visualizaciones y modelado de datos.
* **DAX (Data Analysis Expressions)**: Creación de medidas calculadas personalizadas.
* **Power Query**: Limpieza y preparación de la tabla `ventas_procesadas_pBI`.
* **Python**: Análisis y procesamiento de los datos.

---

## 📐 Lógica y Medidas DAX Principales

### Corrección del Margen de Ganancia (`Margen_Correcto`)
Para corregir el cálculo del porcentaje de margen promedio acumulado cuando los valores numéricos están expresados en base 100, se implementó la siguiente medida en DAX:

```dax
Margen_Correcto = AVERAGE(ventas_procesadas_pBI[Profit_Margin_%]) / 100
