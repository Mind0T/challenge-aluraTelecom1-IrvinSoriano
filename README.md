hola
# 📉 Challenge Data Science - Telecom X (Análisis de Churn)

## 📝 Descripción del Proyecto
Este proyecto es la solución al desafío "Telecom X", enfocado en abordar un problema clásico y crítico en la industria de las telecomunicaciones: la **evasión de clientes (Churn)**. 

El objetivo principal es aplicar técnicas de Extracción, Transformación y Carga (ETL) sobre un conjunto de datos anidado en formato JSON, para luego realizar un Análisis Exploratorio de Datos (EDA). Los hallazgos obtenidos buscan entender qué factores impulsan las cancelaciones y ofrecer recomendaciones estratégicas para mejorar la retención.

## 🛠️ Tecnologías y Herramientas Utilizadas
* **Lenguaje:** Python 3
* **Manipulación y Limpieza de Datos:** `pandas`, `numpy`, `json`
* **Visualización de Datos:** `matplotlib`, `seaborn`
* **Entorno de Desarrollo:** Jupyter Notebook / Google Colab

## 📂 Flujo de Trabajo (Pipeline de Datos)
El proyecto documenta un proceso analítico completo dividido en las siguientes fases:

1. **Extracción:** Carga y aplanamiento (*flattening*) de una base de datos estructurada en JSON anidado utilizando `pd.json_normalize()`.
2. **Transformación (Data Cleaning):** * Detección y corrección de inconsistencias (ej. valores numéricos ocultos como espacios en blanco `' '`).
   * Conversión de tipos de datos (`astype(float)`).
   * Creación de nuevas variables calculadas (Cargos diarios).
   * Estandarización de nombres de columnas.
3. **Carga y Análisis Exploratorio (EDA):**
   * Análisis descriptivo de variables categóricas (contrato, servicio de internet, método de pago) y su relación con el *Churn*.
   * Análisis de distribución de variables numéricas (permanencia, cargos mensuales) mediante *boxplots*.
4. **Análisis de Correlación:** Generación de un mapa de calor (*heatmap*) para entender las relaciones matemáticas entre las variables numéricas y la variable objetivo.

## 💡 Insights y Recomendaciones Principales
El análisis reveló patrones claros de abandono:
* **Contratos:** Los usuarios con pagos de mes a mes (*Month-to-month*) son altamente propensos a cancelar el servicio.
* **Servicio:** El internet por Fibra Óptica presenta una tasa de cancelación anormalmente alta comparada con el ADSL.
* **Facturación:** Los clientes que pagan sumas mensuales más altas y utilizan cheques electrónicos (*Electronic check*) lideran la fuga.
* **Permanencia:** La mayor tasa de abandono ocurre en los primeros meses de servicio.

**Acciones sugeridas:** Diseñar campañas para incentivar la migración a contratos anuales, auditar urgentemente la calidad/precio de la Fibra Óptica y crear un programa de fidelización focalizado en los primeros meses de vida del cliente.

## 🚀 Cómo ejecutar el proyecto
1. Clona este repositorio en tu máquina local.
2. Asegúrate de tener instaladas las dependencias: `pip install pandas numpy matplotlib seaborn`
3. Abre el archivo `TelecomX_LATAM_IrvinSoriano.ipynb` en Jupyter Notebook o Google Colab.
4. Asegúrate de que el archivo `TelecomX_Data.json` esté en la misma ruta que el notebook.
5. Ejecuta las celdas para reproducir el proceso ETL y visualizar los gráficos.

---

## 👨‍💻 Autor

**Irving Soriano** | Estudiante de la Licenciatura en Ciencia de Datos en ESCOM (IPN).

📫 **Contacto y Redes:**
* **LinkedIn:** [Irving Soriano](https://www.linkedin.com/in/irving-soriano)