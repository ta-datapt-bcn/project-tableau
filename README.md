![IronHack Logo](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_d5c5793015fec3be28a63c4fa3dd4d55.png)

# Project: 2020 Spotify Trends

## Overview

El objetivo de este proyecto es el de estudiar las tendencias mas populares e influyentes de la música a lo largo 2020 en España a través de Spotify. Spotify es una aplicación multiplataforma sueca, empleada para la reproducción de música vía streaming, que pone a disposición de los desarrolladores su API de acceso público. Además de contar con la pagina web https://spotifycharts.com/regional donde quedan registradas las top 200 canciones mas escuchadas de cada día del año.

De la plataforma Genius, que cuenta con una de las más grandes colecciones de canciones del mundo, se extraerán las letras de todas las canciones del top 200 de 2020.

La primera parte del proyecto consistirá en la extracción de toda información de estas fuentes y una primera limpieza de los datos obtenidos. Esta información se subirá a la plataforma Big Query, el Data Warehouse de Google, integrado por Google Cloud donde se alojará nuestro dataset. Este Dataset estará formado por 3 tablas que se manipularán y limpiaran en Google Cloud para generar las tablas que se utilizarán para la visualición en Tableau. 

---

## Data Sources

Los 3 principales fuentes de información para este proyecto han sido: Spotify Charts, la API de Spotify y lyricsgenius.

Spotify Charts es una pagina web en donde para cada dia del año de cada país del mundo Spotify muestra las top 200 canciones mas stremeadas. La información disponible consiste de el nombre de la canción, artista, streams y la fecha. Esta información se obtendrá mediante el scrapeo de la página web utilizando BeautifulSoup.

Para complementar Spotify Charts se utilizará la API de Spotify donde se encuentran disponible: una id, nombre, artista, el genero de las canciones y las propiedades que define Spotify para estas.

Finalmente para se obtendrán las letras de todas estas canciones mediante lyricsgenius, que es un cliente para Python para la API de Genius, que utiliza el scrapeo web para la obtención de estas letras.

## Google Big Query

Esta información se subirá a la plataforma Big Query, el Data Warehouse de Google, integrado por Google Cloud donde se alojará nuestro dataset. Este Dataset estará formado por 3 tablas que se manipularán y limpiaran en Google Cloud para generar las tablas que se utilizarán para la visualición en Tableau. 


## Data Treament

De la manipulación de los datos hecha en Google Cloud se obtiene la principal tabla del Dataset que aglomera toda la información relevante del proyecto, AnnualReport. En esta tabla se ven reflejados la fecha, cancion, streams, artistas, generos, las propiedades de las canciones y el conteo de palabras.

La tabla SongProperties se genera mediante AnnualReport en donde para cada canción se indican las propiedades de estas.

Finalmente la tabla WordCount es un diccionario, donde para todo el conjunto de las canciones de 2020, se cuentan las palabras mas utilizadas. El proceso de conteo de palabras consistió en primero limpiar las letras obtenidas de falsos positivos, mayusculas, puntuación, acentos y Stopwords. A continuación se genera un Bag of Words para cada uno de las canciones que finalmente se suman todas para generar el diccionario final.

## Visualization

La información obtenida se utiliza para generar con Tableau una serie de gráficos en los que se estudia las tendencias musicales de 2020. Estos gráficos son del tipo treemap, burbujas, lineales y radar.

Para el analisis de las palabras se realiza un WordCloud que se genera mediante la pagina web https://wordart.com/.




