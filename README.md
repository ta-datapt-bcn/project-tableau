![IronHack Logo](https://s3-eu-west-1.amazonaws.com/ih-materials/uploads/upload_d5c5793015fec3be28a63c4fa3dd4d55.png)

# Proyecto: Business Intelligence with Tableau

## Overview

El objetivo de este proyecto es hacer un análisis para ver cuál sería el mejor barrio para construir pisos de alquiler social. 

## Datos utilizados

Para hacer este anális hemos utilizado datos extraídos de (https://opendata-ajuntament.barcelona.cat/es/) y de (https://ajuntament.barcelona.cat/estadistica/catala/index.htm). Los datos extraídos han sido: 

* Resultados electorales por barrios de las elecciones locales de mayo de 2019 
* Nacionalidades por barrios en enero de 2020 (es el último dato registrado)
* % de población en paro  mensual por barrio en 2021 & 2019
* CSV propio con información de diferentes pisos en BCN (precio, m2, etc...)
* Un geojson con los barrions (polígonos) de BArcelona 

Estos datos los hemos subido a DB Browser y hemos creado una base de datos (Barcelona). Dentro de esta hemos creado tres tablas más: 

- Paro_Abril_2019: Hemos filtrado el dataset del paro mensual 2019 y hemos cogido solo el detalle del mes de abril, con el objetivo de poderlo comparar con el resultado electoral de mayo 2019 
- Paro_Marzo_2021: Hemos filtrado el dataset del paro mensual 2021 y hemos cogido el detalle del mes más reciente (para poder ver la distribución por barrios del paro en un Heat Map
- Partido ganador: Hemos filtrado el dataset de los Resultados electorales y hemos creado una tabla con el partido más votado por barrio. 

Finalmente hemos exportado todas las tablas que necesitábamos en formato csv y las hemos subido a Tableau. 

## Hemos presentado los datos en tableau: 

https://public.tableau.com/profile/gloria1001#!/vizhome/DesigualdadesenBarcelona_16204601428370/DesigualdadesenBCN

Hemos creado 4 Heat Maps para ver la distribución por barrios de: 

* Precios de alquiler por barrio
* Nº de extranjeros por barrio 
* % Parados por barrio 
* Número de extranjeros por barrio 

También hemos creado un diagrama de barras para comparar el % de parados por barrio y el partido más votado

Finalmente hemos creado un scatter plot para comparar el precio medio por pisos con el % de paro. 

## Conclusión a la que hemos llegado: 

Si tuviéramos que construir pisos de alquiler social los construiríamos en Torre Baró, donde los precios de los pisos son altos, el número de parados también y la población extranjera también. 

## Problemas encontrados: 

Hemos tenido muchos problemas a la hora de subir los datasets a tableau, hemos perdido más tiempo intentando subir los documentos y connectarlos entre ellos,  que haciendo las visualizaciones. 

## ¿Qué he aprendido?

Este proyecto ha sido útil para aprender a trabajar con Tableau y practicar SQL. He aprendido que a la hora de analizar los datos hay que ser más críticos y tener en cuenta más datos (ejemplo: en el diagrama de barras en el que comparábamos el % de parados con el partido más votado, tendríamos que haber tenido en cuenta la media de edad de cada barrrio)
