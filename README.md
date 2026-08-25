# Retail-Maintenance-Logistics-Budget-Audit-Acapulco-Iguala-
# 🛠️ Audit & Financial Control of Field Expenses: Coppel Guerrero Project

## 📌 Descripción del Proyecto
Este proyecto analiza la gestión logística, el control de viáticos y la ejecución financiera de una cuadrilla de mantenimiento asignada a **10 solicitudes de trabajo (Work Orders)** para **Coppel** en el estado de Guerrero (abril - mayo de 2026). Con un presupuesto asignado de **$250,000.00 MXN**, el proyecto evalúa la distribución de gastos en 8 sedes clave en **Acapulco** (*Tienda Bahía, Renacimiento, Pie de la Cuesta, Oficinas de Cobranza 1 y 2, Estacionamiento y CEDIS 1*) e **Iguala** (*Tienda Tamarindos*).

El objetivo principal fue auditar **135 comprobantes y tickets de gasto** para cuantificar desviaciones presupuestales, evaluar la sobrecostos por compras locales de emergencia y calcular la proporción entre gasto operativo directo vs. viáticos y traslado.

---

## 📊 Preguntas de Negocio Resueltas

1. **Control Presupuestal:** ¿El proyecto se mantuvo dentro del límite programado de $250,000 MXN o existieron desviaciones significativas al cierre de mayo?
2. **Impacto Logístico vs. Insumos:** ¿Qué porcentaje del presupuesto se consumió en traslados y viáticos (Autopista del Sol, Pemex, hoteles) frente a la compra efectiva de materiales de obra?
3. **Fuga Financiera por Compras Locales:** ¿Cuál fue el impacto económico y el porcentaje de sobrecosto por adquirir materiales en ferreterías locales y Home Depot Acapulco en lugar de surtir desde el stock central de CDMX?
4. **Concentración por Sede:** ¿Qué inmuebles concentraron la mayor cantidad de comprobantes y desviaciones monetarias?

---

## 📈 Hallazgos Clave & Insights de Negocio

* **Centro de Gravitación Operativo:** **Tienda Bahía** en Acapulco concentró la mayor carga operativa con **32 comprobantes (23.7% del total de registros)**, seguida de Tienda Renacimiento (22 comprobantes).
* **Sobrecostos por Compras de Emergencia:** Aunque las compras centralizadas desde CDMX (54 registros) mantuvieron una variación controlada (<2%), las **19 compras de emergencia en ferreterías de Acapulco** registraron **sobrecostos del 15% al 32%** sobre el presupuesto unitario estimado.
* **Carga de Soporte Logístico:** Los viáticos y la logística de traslado (peajes en Autopista del Sol, gasolina y hospedaje) representaron **62 de los 135 comprobantes (45.9% del volumen documental)**, evidenciando el alto costo fijo asociado a la atención de proyectos foráneos.
* **Calidad de Datos:** Auditoría completada sobre 135 comprobantes con **0% de registros nulos y 0 duplicados**, asegurando trazabilidad completa sobre las 10 Work Orders asignadas.

---

## 🛠️ Tecnologías y Herramientas Utilizadas

* **Lenguaje:** Python 3.x
* **Librerías de Análisis:** Pandas, NumPy
* **Visualización:** Matplotlib, Seaborn
* **Entorno de Desarrollo:** Google Colab / Jupyter Notebooks

---

## 🔄 Flujo del Proyecto (ETL & EDA)

1. **Carga y Verificación de Integridad:** Validación de dimensiones (135 filas × 9 columnas), confirmación de ausencia de valores nulos/duplicados y análisis de cardinalidad sobre las 10 Work Orders y 8 sedes.
2. **Transformación & Tipado:** Conversión de la variable `Fecha` de formato `object` a `datetime` para habilitar el agrupamiento temporal entre abril y mayo de 2026.
3. **Ingeniería de Características Financieras:**
   * Cálculo de Variación Absoluta ($): `Gasto_Real_MXN - Presupuesto_Asignado_MXN`.
   * Porcentaje de Variación (%): `(Variacion_MXN / Presupuesto_Asignado_MXN) * 100`.
   * Etiquetado de estatus presupuestal (*Sobrecosto* vs. *Ahorro*).
4. **Análisis Estadístico Descriptivo:** Evaluación de tendencia central (media y mediana) y dispersión financiera por categoría de gasto.

---

## 📁 Estructura del Repositorio

```text
├── data/
│   ├── proyecto_guerrero_coppel.csv   # Dataset original de gastos comprobados
│   └── guerrero_preparado.csv         # Dataset procesado con variables financieras
├── notebooks/
│   └── Auditoria_Viaticos_Guerrero.ipynb # Notebook interactivo en Google Colab
└── README.md                          # Documentación del proyecto
