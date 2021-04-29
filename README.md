# MODELOS DE PREDICCIÓN
El objetivo general de este proyecto es armar un modelo sencillo para predecir el precio de propiedades en dólares, utilizando DecisionTreeRegressor y KNeighborsRegressor de Scikit-learn. El objetivo específico es lograr mayor precisión en la predicción del modelo, para ello se trabaja en el ajuste de los parámetros y su evaluación. La métrica utilizada es RMSE (raíz del error cuadrático medio) y se trabaja sobre un Dataset sobre propiedades a la venta, el cual ya ha sido limpiado.

Para lograr este objetivo se realizan los siguientes pasos:
-	Descripción de nuevos atributos que serán analizados.
-	Importación de las bibliotecas necesarias para la exploración. Para este análisis se trabajará con Scikit-learn, Pandas, Numpy, Seaborn y MatplotLib.pylab.
-	Carga, lectura y observación de la cantidad de instancias contenidas en el Dataset.
-	División del dataset en conjunto de entrenamiento, para el cual será utilizado el 80% de los datos y conjunto de testeo con el restante 20%.
### Decision Tree
-	Cálculo del RMSE (root mean square error) para ser utilizado como métrica. Medición del MSE (mean_squared_error) y obtención su raíz cuadrada.
-	Entrenamiento del conjunto de training con el DecisionTreeRegressor desde la librería sklearn.tree.
-	Predicción sobre el conjunto de test y creación de variable para guardar el resultado.
-	Análisis del cambio en el RMSE a medida que se profundiza en el árbol de decisión, tanto en training como en testing, para ello se itera de 5 en 5 el parámetro 'max_depth' y se observa el impacto.
-	Visualización gráfica de la comparación entre los resultados obtenidos de RMSE en training y testing, con la variación de la profundidad mediante pyplot de MatPLotLib.
-	Conclusiones del modelo.
### K-Nearest Neighbors
-	Cálculo del RMSE (root mean square error) para ser utilizado como métrica. Medición del MSE (mean_squared_error) y obtención su raíz cuadrada.
-	Entrenamiento del conjunto de training con el k-NearestNeighbors desde la librería sklearn.neighbors.
-	Predicción sobre el conjunto de test y creación de variable para guardar el resultado.
-	Análisis del cambio en el RMSE a medida que son considerados más vecinos para KNN, tanto en training como en testing. Para esto, se itera incrementando de a uno el parámetro 'n_neighbors' y se observa el impacto.
-	Se repite el proceso con los arreglos 'rmses_train' y 'rmses_test' para cada profundidad y se grafican con pyplot de MatPLotLib.
-	Conclusiones del modelo.
### Cross Validation
-	Calculo del RMSE promedio con Cross Validation para un árbol de decisión con parámetros definidos.
-	Reentrenamiento del regresor y visualización de los resultados de la comparación entre los valores reales, los predichos y su diferencia, por medio de un DataFrame.
