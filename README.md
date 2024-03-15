
## Proyecto 2 Bootcamp en Data Science: Recomendador de Spotify

Para la realización de este segundo proyecto hemos partido de un dataset de Kaggle:

https://www.kaggle.com/datasets/tonygordonjr/spotify-dataset-2023

De este dataset, hemos utilizado el fichero que se llama spotify_data_12_20_2023.csv 

Lo primero que hicimos fue echar un vistazo a cómo estaban los datos: qué columnas tenía, sí tenía NANs, qué tipo de datos contenían las columnas, etc.

Fuimos analizando una a una las columnas del fichero para ver cuáles eran los datos que nos iban a interesar y así creamos un DataFrame con las columnas y la información que consideramos relevante.

Para empezar graficamos con matplotlib la distribución entre los followers y los artistas:


![image](https://github.com/triche31/proyecto2_datascience/assets/155429359/1f666678-6dab-41eb-a5c5-95c2f81a46bc)

Continuamos con la creación de la función que nos va a servir para este recomendador que lo que hace es pedirle al usuario que introduzca el nombre de un artista o banda y que lo puntúe.

Parara poder hacer este recomendador necesitamos información de usuarios y sus puntuaciones a los artistas, como no disponemos de esa información, lo qe hacemos es generarla de forma ficticia, de tal forma que al final dispondremos de una serie de usuarios, con sus puntuaciones y el id de los artistas que han puntuado. 

El fichero usuarios.csv es un fichero que se ha generado con esa información ficticia de los usuarios.

Definimos lo que sería nuestro usuario activo donde utilizaremos la función mencionada antes para tener los datos de puntuación de artistas que el usuario nos está indicando.

A continuación, realizamos distintas operaciones para establecer los campos que vamos a utilizar para poder generar las recomendaciones en función de los artistas y puntuaciones otorgados por el usuario activo. 

Este último DataFrame tendrá los campos iniciales más los siguientes: 
- weigh
- similitud
- final

Donde weigh son las puntuaciones que tenemos del usuario por la similutd que posee con el usuario activo.

La similitud es el coseno de similitud de las puntuaciones proporcionadas por el usuario activo.

Y la columna final es la división entre weigh y la similitud.

En nuestro caso hemos puesto los siguientes artistas con estas puntuaciones:

![image](https://github.com/triche31/proyecto2_datascience/assets/155429359/9e70815d-cd7c-46c1-a314-4475ed659efd)

Y como resultado nos salen estos tres artistas recomendados:

![image](https://github.com/triche31/proyecto2_datascience/assets/155429359/846e845c-8d3a-47e4-9f0b-3673da3603e0)


Para terminar con la parte de recomendación, lo que hacemos es de los artistas que hemos recomendado previamente, sacamos un sample de 10 canciones, en las que habrá artistas repetidos. En nuestro caso tenemos lo siguiente:

![image](https://github.com/triche31/proyecto2_datascience/assets/155429359/c6ddc5ea-f9d7-4435-b30b-c97ed6a00beb)

Acabamos el proyecto dando una serie de visualizaciones como pueden ser las siguientes: 

#### Gráfico genero (elección usuario-recomendador) 

![image](https://github.com/triche31/proyecto2_datascience/assets/155429359/e8245f40-9f69-4c53-8188-fb0bdb52175e)

#### Gráfico canciones recomendadas vs loudness de esas canciones

![image](https://github.com/triche31/proyecto2_datascience/assets/155429359/955f6c42-89fd-4dfc-bef0-b8dbadbcc690)



## Authors

- [@aidamoo](https://www.github.com/aidamoo)
- [@Esthergg93](https://www.github.com/Esthergg93)
- [@e-velazco](https://www.github.com/e-velazco)


