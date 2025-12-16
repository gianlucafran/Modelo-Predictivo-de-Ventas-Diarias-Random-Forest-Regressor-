# 📈 Modelo Predictivo de Ventas Diarias (Random Forest Regressor)

## Resumen del Proyecto

Este proyecto implementa un modelo de Machine Learning (Random Forest Regressor) para pronosticar las ventas diarias con una **precisión del 99% ($R^2=0.9902$)**. El análisis confirma que la demanda es impulsada casi exclusivamente por factores temporales, proporcionando una herramienta de alta fiabilidad para la optimización operativa y la planificación de inventario.

## 🎯 Conclusiones Clave

1.  **Alta Predictibilidad:** Las ventas son altamente predecibles (R2 = 0.9902).
2.  **Motores de Demanda:**
    * **Día de la Semana:** Factor dominante ($\approx 82\%$ de importancia). La demanda crece linealmente de Lunes a Domingo.
    * **Festivo:** Factor modulador fuerte ($\approx 18\%$ de importancia).
3.  **Inefectividad:** La variable `Promociones` demostró ser insignificante ($\approx 0.1\%$ de importancia), sugiriendo una reevaluación de su impacto.
4.  **Mecánica del Modelo:** El modelo predice en **saltos discretos (escalones)**, reflejando la discontinuidad real de la demanda entre las categorías de días, lo cual es capturado de manera efectiva por el Random Forest.

## 🛠️ Estructura del Repositorio

* `data/`: Contiene el set de datos inicial (`df_nuevo.csv`).
* `notebooks/`: Archivo Jupyter Notebook con el código completo.
    * `Ventas_Prediccion.ipynb`: ETL, EDA, Feature Engineering, Entrenamiento del Random Forest y Evaluación.
* `model/`: Carpeta donde se guarda el modelo final (`rf_model.pkl`) para su despliegue futuro.
* `requirements.txt`: Lista de dependencias de Python (Pandas, Scikit-learn, Matplotlib, Seaborn, Numpy).

## 🚀 Cómo Ejecutar el Proyecto

1.  **Clonar el Repositorio:**
    ```bash
    git clone [URL_DE_TU_REPOSITORIO]
    cd ModeloPredictivoVentas
    ```
2.  **Instalar Dependencias:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Ejecutar el Notebook:** Abrir `Ventas_Prediccion.ipynb` con Jupyter Lab/Notebook y ejecutar las celdas secuencialmente.

## 📈 Visualizaciones Clave

* **Distribución de Ventas por Día de la Semana:** Muestra el patrón ascendente de Lunes a Domingo. 
* **Ventas Reales vs. Predichas:** Muestra la alineación perfecta en escalones, probando la alta precisión del modelo. 
* **Importancia de Características:** Gráfico de barras que confirma la preponderancia de `DíaDeLaSemana` sobre el resto de variables.
