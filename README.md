# Analysis-novaretail
Análisis exploratorio de datos y modelado de correlación estadística (Pearson, Spearman, Punto-Biserial, V de Cramér) sobre el comportamiento de compra, efectividad publicitaria y adopción de programas de suscripción en NovaRetail+.
# 📊 Análisis de Correlación y Comportamiento del Consumidor en NovaRetail+

Este proyecto realiza un **Análisis Exploratorio de Datos (EDA)** y evalúa las relaciones estadísticas entre variables demográficas, operativas y de segmentación en un conjunto de datos de **15,000 usuarios** de la plataforma NovaRetail+. 

El objetivo principal es identificar los motores clave que impulsan el **ingreso anual** por cliente y evaluar la eficiencia de las estrategias de marketing personalizado y programas de fidelidad.

---

## 🎯 Objetivos del Proyecto
* **Identificar factores de valor:** Determinar cuáles variables numéricas y categóricas muestran una asociación significativa con los ingresos reales generados.
* **Evaluar canales de marketing:** Medir la correlación entre la inversión en publicidad dirigida y el retorno financiero por usuario.
* **Analizar segmentación de clientes:** Estudiar si el comportamiento de compra o la elección tecnológica varía según la distribución geográfica.
* **Sustentación metodológica:** Aplicar el coeficiente de correlación adecuado según la naturaleza y escala de medición de cada variable.

---

## 🛠️ Metodología Estadística Aplicada

Para garantizar la precisión técnica, el análisis se dividió según el tipo de datos:

1. **Variables Numéricas Continuas (Matriz de Correlación / Heatmap):** Se utilizó el coeficiente de **Pearson** para identificar dependencias lineales y descartar problemas de colinealidad.
2. **Relaciones No Lineales o de Rango:** Se aplicó el coeficiente de **Spearman** para evaluar variables ordinales o con distribuciones asimétricas (como los niveles de satisfacción).
3. **Variables Numéricas vs. Variables Binarias (0/1):** Se implementó el coeficiente **Punto-Biserial** para medir el impacto de la condición de suscripción (`miembro_premium`) y la deserción (`abandono`) sobre el gasto total.
4. **Variables Categóricas Nominales (Texto vs. Texto):** Se construyó una función personalizada basada en tablas de contingencia (frecuencias cruzadas) y pruebas de Chi-cuadrado para calcular la **V de Cramér**, evaluando la asociación entre `tipo_dispositivo` y `region`.

---

## 🚀 Principales Hallazgos de Negocio

* **El Programa Premium como Motor de Valor:** El análisis numérico confirmó una fuerte relación positiva (Punto-Biserial $\approx$ 0.65) entre los usuarios con suscripción activa y los mayores niveles de ingreso anual. Esto resalta la importancia de diseñar estrategias de conversión hacia este segmento.
* **Publicidad Dirigida Eficiente:** Se identificó una correlación lineal positiva moderada (Pearson $\approx$ 0.52) respecto al gasto en publicidad personalizada, demostrando que la inversión en marketing digital está alineada con el incremento en las ventas.
* **Homogeneidad Tecnológica Regional:** La asociación entre la región geográfica del cliente y el dispositivo de acceso fue prácticamente nula (V de Cramér $\le$ 0.05). Los patrones de adopción móvil son consistentes en todo el país, lo que valida el uso de una estrategia de optimización web/app global.
* **Límite Analítico (Correlación ≠ Causalidad):** Se estableció como limitación metodológica que los coeficientes demuestran la fuerza de la asociación en un corte transversal del tiempo, pero no determinan causalidad directa ni contemplan variables externas de estacionalidad o competencia.

---

## 💻 Tecnologías Utilizadas
* **Python 3.9+**
* **Pandas** & **NumPy** (Manipulación y estructuración de datos)
* **Matplotlib** & **Seaborn** (Visualización estática y matrices de calor)
* **SciPy (scipy.stats)** (Cálculo de significancia estadística, p-valores y Chi-cuadrado)
* **Jupyter Notebooks** (Entorno de desarrollo e informes)

---

## 📂 Estructura del Repositorio
* `S8 Student Version-Project-NovaRetail.ipynb`: Notebook principal con el desarrollo del código, carga del dataframe, cálculo de coeficientes y visualizaciones de dispersión.
* `README.md`: Documentación del proyecto.
