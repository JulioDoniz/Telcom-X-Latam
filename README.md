1.  **Cargar Datos**: Lee los datos de los clientes desde un archivo JSON alojado en GitHub.
2.  **Exploración de Datos**: Muestra el encabezado (`head`) y la información (`info`) del dataframe para obtener una comprensión básica de la estructura y tipos de datos.
3.  **Transformación de Datos**:
    * Expande las columnas JSON anidadas (`customer`, `phone`, `account`, `internet`) en columnas separadas.
    * Renombra columnas para mejorar la legibilidad (`gender` a `Gender`, `tenure` a `Tenure`, `customerID` a `CustomerID`).
    * Convierte columnas relevantes a tipos numéricos (`Charges.Total`, `Charges.Monthly`).
    * Crea una nueva columna `DailyCharges` dividiendo `ChargesMonthly` por 30.
    * Convierte columnas categóricas binarias (`Partner`, `Dependents`, `PhoneService`, `PaperlessBilling`, `MultipleLines`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`) a representación numérica (1 para 'Yes', 0 para 'No').
    * Maneja 'No phone service' en `MultipleLines` reemplazándolo con 'No'.
    * Identifica y cuenta los diferentes valores en la columna **'Churn'**, incluyendo 'Yes', 'No' y 'N/A'.
4.  **Visualización de Datos**:
    * Genera un gráfico de pastel (**pie chart**) que muestra la proporción de clientes que rotaron, no rotaron y aquellos con estado de rotación 'N/A'.
    * Crea un mapa de calor (**heatmap**) para visualizar el recuento de clientes que rotaron basado en la combinación de 'Gender', 'Contract' y 'InternetService'.
    * Genera diagramas de caja (**box plots**) para mostrar la distribución de 'ChargesMonthly' y 'Tenure' para los clientes basándose en su estado de rotación.
5.  **Guardar Datos**: Guarda el dataframe procesado en un nuevo archivo JSON llamado `Churn_de_Clientes.json`.

---

## Cómo Usar

1.  **Abrir el notebook**: Abre este Jupyter Notebook en un entorno compatible (como Google Colab).
2.  **Ejecutar las celdas**: Ejecuta cada celda de código secuencialmente.
3.  **Inspeccionar la salida**: Revisa la salida de cada celda, incluyendo los dataframes impresos y los gráficos generados, para comprender los datos y el análisis realizado.
4.  **Acceder a los datos procesados**: Los datos procesados con las transformaciones aplicadas se guardarán como `Churn_de_Clientes.json` en el mismo directorio que el notebook. Puedes descargar y usar este archivo para análisis o modelado adicionales.

---

## Dependencias

El notebook utiliza las siguientes bibliotecas de Python:

* `pandas` para manipulación y análisis de datos.
* `requests` para obtener datos de la web.
* `matplotlib.pyplot` para crear visualizaciones.
* `seaborn` para visualizaciones estadísticas mejoradas.
* `matplotlib.colors.LinearSegmentedColormap` para crear mapas de color personalizados.

Asegúrate de tener estas bibliotecas instaladas en tu entorno. Si estás utilizando Google Colab, estas bibliotecas suelen estar preinstaladas.
