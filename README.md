# Proyecto_Individual_1_Henry
Proyecto Individual n°1 - Henry - Machine Learning Operations (MLOps)

## Proyecto de recomendación de películas
Este repositorio contiene el código y los recursos necesarios para implementar un sistema de recomendación de películas. El objetivo principal es desarrollar un modelo de Machine Learning que pueda proporcionar recomendaciones personalizadas a los usuarios en función de sus preferencias y comportamientos pasados.

El proyecto se divide en tres etapas principales: ETL (Extracción, Transformación y Carga), EDA (Análisis Exploratorio de Datos) y ML (Aprendizaje Automático),y una API para interactuar con el modelo de recomendación.

### ETL (Extracción, Transformación y Carga)
En esta etapa, el objetivo es realizar el procesamiento y la preparación de los datos necesarios para el entrenamiento del modelo de recomendación. El trabajo del Data Engineer es crucial en esta fase, ya que los datos iniciales pueden estar desorganizados, anidados o sin procesar. El proceso de ETL implicó las siguientes tareas:
- Extracción: Obtención de los datos de 2 archivos CSV, con un archivo de diccionario para la comprensión de algunas variables. Dentro de los dataset encontramos información sobre películas, usuarios, calificaciones, géneros, etc. 
- Transformación: Realización de tareas de limpieza y transformación de los datos extraídos. Para esto se siguieron las pautas propuestas en la consigna. Esto incluyó la eliminación de datos faltantes y nulos, la conversión de formatos, la creación de columnas adicionales, entre otros.
- Carga: para el almacenamiento de los datos procesados se usaron archivos csv y eventualmente se buscaron herramientas para trabajar con datos .zip.

### API para interacción: 
Se ha implementado una API utilizando FastAPI y Python para interactuar con el sistema. La API proporciona diferentes consultas y funcionalidades para obtener información sobre las películas y actores, cada una de ellas con un decorador (@app.get(‘/’)). A continuación se describen las principales consultas disponibles:
1. Cantidad de filmaciones por mes:
   Descripción: Esta consulta devuelve la cantidad de películas que fueron estrenadas en el mes especificado en el dataset.
2. Cantidad de filmaciones por día:
   Descripción: Esta consulta devuelve la cantidad de películas que fueron estrenadas en el día especificado en el dataset.
3. Score de una película: 
   Descripción: Esta consulta devuelve el título de la película, el año de estreno y el score/popularidad de la película especificada.
4. Votos de una película: 
   Descripción: Esta consulta devuelve el título de la película, la cantidad de votos y el valor promedio de las votaciones. Si la película tiene menos de 2000 valoraciones, se devuelve un mensaje indicando que no cumple con esta condición.
5. Información de un actor:
   Descripción: Esta consulta devuelve información sobre un actor específico. Incluye la cantidad de películas en las que ha participado, el éxito medido a través del retorno y el promedio de retorno por filmación. Esta definición no considera a los directores.
6. Información de un director:
   Descripción: Esta consulta devuelve información sobre un director específico. Incluye el éxito del director medido a través del retorno, el nombre de cada película dirigida por él/ella, la fecha de lanzamiento, el retorno individual, el costo y la ganancia de cada película.

Estas consultas están diseñadas para proporcionar información relevante y útil sobre las películas, actores y directores en el dataset. Al utilizar la API, podrás acceder a estas funcionalidades y obtener respuestas personalizadas según los parámetros que se ingresen. 
 
### EDA (Análisis Exploratorio de Datos)
Una vez que los datos han sido preparados y cargados, se realiza un análisis exploratorio para comprender mejor las características y patrones presentes en los datos. El EDA permite obtener información valiosa que ayudará a tomar decisiones sobre el diseño y entrenamiento del modelo de recomendación. Algunas tareas realizadas en esta etapa son:

- Visualización de datos: Creación de gráficos, histogramas y otras visualizaciones para explorar las relaciones entre las variables y comprender la distribución de los datos.
- Análisis de correlación: Evaluación de la correlación entre algunas variables de interés. Esto ayuda a identificar algunas características pueden ser más relevantes para el modelo de recomendación y poder eventualmente profundizar en el análisis del dataset.

### ML (Aprendizaje Automático)
En esta etapa, se desarrolla el modelo de recomendación utilizando la técnica de TF-ID (Term Frequency-Inverse Document Frequency) la cual es comunmente utilizada para medir la importancia de un término en un documento, como en tareas de procesamiento de lenguaje natural. El objetivo era encontrar un modelo capaz de recomendar películas, en el caso de esta técnica, basado en la variable "overview". 

## Ejecución en Render.com
Dentro de este repositorio se el código (main) y los recursos (requirements.txt) necesarios para implementar una API en Render.com. La API previamente generada devolverá en el servidor las consultas seteadas y desarrolladas previamente.
El enlace para acceder al mismo es: https://proyecto-individual-1-aglg.onrender.com

## Explicación del proyecto
El desarrollo del proyecto se encuentra en un video de Youtube a través del siguiente enlace: youtu.be/ZPTy6uWifOk 

El presente proyecto se encuentra abierto a recomendaciones y futuras modificaciones.

Los datasets originales se encuentran disponibles en: https://drive.google.com/drive/folders/1l1wkloKC-U1qoW_sjGXJpcVQI32OXvRH?usp=sharing
