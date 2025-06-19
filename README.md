# clasificadorimagenes
El objetivo del trabajo fue implementar y evaluar modelos de clasificación supervisada (KNN y Random Forest) aplicados a imágenes multiespectrales Sentinel-2, con el fin de identificar diferentes coberturas del suelo. Se trabajó con dos recortes de una imagen satelital obtenida y procesada previamente en QGIS. 
El pipeline completo abarca desde la carga y visualización de la imagen satelital, el procesamiento y recorte de zonas de interés, hasta la extracción de muestras y entrenamiento/evaluación de clasificadores.

🗂️ Principales Componentes del Proyecto
1. Carga y visualización de imagen Sentinel-2
Uso de rasterio para manejar archivos raster.
Visualización de bandas y generación de RGB a partir de bandas multiespectrales.

2. Preprocesamiento y Recorte
Recortes definidos mediante polígonos cargados desde archivos Geopackage generados en QGIS.
Escalado de bandas con técnicas de ecualización por percentiles.

3. Extracción y generación de muestras
Utilización de clases personalizadas en Python para crear datasets de entrenamiento.
Etiquetado basado en polígonos con clases previamente definidas.

4. Modelado
Entrenamiento y validación de dos modelos:
K-Nearest Neighbors (KNN)
Random Forest (RF)

Cálculo de métricas:
Matriz de confusión
Accuracy, precision, recall, F1-score

5. Evaluación sobre un nuevo recorte
Aplicación de los modelos entrenados al segundo recorte no visto durante el entrenamiento.
Evaluación de la generalización con nuevas muestras.

🧰 Tecnologías y Librerías Utilizadas
Python
rasterio, shapely, geopandas
scikit-learn
matplotlib, seaborn
NumPy, Pandas

📊 Resultados:
Ambos modelos lograron buenos desempeños en la clasificación de coberturas del suelo.
El modelo de Random Forest mostró una mejor capacidad de generalización en comparación con KNN al aplicarse sobre un recorte no visto.
Se visualizó y analizó la distribución espacial de las clases predichas en los mapas generados.
