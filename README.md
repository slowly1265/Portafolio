Pronóstico Macroeconómico con Machine Learning
Trabajo de portafolio semestral — Ciencia de Datos para la Economía, Ingeniería Comercial
(UDP).
Réplica y extensión del paper:
Goulet Coulombe, P., Leroux, M., Stevanovic, D., & Surprenant, S. (2022). How is
machine learning useful for macroeconomic forecasting? Journal of Applied
Econometrics, 37(5), 920–964. 
https://doi.org/10.1002/jae.2910
Descripción del proyecto
Este proyecto compara distintos modelos de Machine Learning aplicados al pronóstico de
variables macroeconómicas de Estados Unidos, usando la base de datos FRED-MD
(McCracken & Ng, 2016).
Se replican los modelos principales del paper original —ARDI (regresión lineal sobre
componentes principales), Ridge, Lasso, ElasticNet y Random Forest— y se propone un
modelo adicional no considerado por los autores: XGBoost, para evaluar si el boosting
secuencial aporta ventajas sobre el bagging del Random Forest.
Variables objetivo:
INDPRO — Producción industrial
UNRATE — Tasa de desempleo
Horizontes de pronóstico: 1, 3 y 12 meses
Métricas de evaluación: RMSE (principal), MAE, R²
Estructura del repositorio
├── Portafolio_Ciencias_Datos.ipynb   # Cuaderno principal con todo el análisis
├── README.md                         # Este archivo
├── requirements.txt                  # Dependencias del proyecto
└── presentacion/                     # (opcional) Slides y guion de la exposición
Estructura del cuaderno
1. Resumen del paper
2. Datos (descarga de FRED-MD y análisis exploratorio)
3. Preprocesamiento e ingeniería de atributos (transformaciones, imputación, PCA)
4. Modelos del paper (ARDI, Ridge, Lasso, ElasticNet, Random Forest)
5. Modelo adicional propuesto (XGBoost)
6. Comparación de resultados
7. Discusión y conclusiones
Fuente de datos
Los datos se descargan directamente desde el notebook, sin necesidad de archivos
adicionales, desde el sitio oficial de la Reserva Federal de St. Louis:
https://www.stlouisfed.org/-/media/project/frbstl/stlouisfed/research/fred-md/monthly/current.csv
No se requiere ninguna clave de API ni registro previo.
Instrucciones de ejecución
1. Clonar el repositorio
git clone <URL-del-repositorio>
cd <nombre-del-repositorio>
2. Crear un entorno virtual (recomendado)
python -m venv venv
source venv/bin/activate      # En Windows: venv\Scripts\activate
3. Instalar dependencias
pip install -r requirements.txt
4. Ejecutar el notebook
jupyter notebook Portafolio_Ciencias_Datos.ipynb
O bien, subir el archivo .ipynb directamente a 
Google Colab y ejecutar todas las celdas en
orden ( Entorno de ejecución → Ejecutar todas ). El notebook instala automáticamente las
librerías necesarias en la primera celda.
Dependencias principales
pandas , numpy — manipulación de datos
matplotlib , seaborn , missingno — visualización
scikit-learn — modelos lineales, Random Forest, PCA, validación cruzada
xgboost — modelo adicional propuesto
Ver requirements.txt para la lista completa.
