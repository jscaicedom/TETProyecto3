# Proyecto 3 Big Data
## Por: Alejandro Arroyave Bedoya - Johanna Saraí Caicedo Mejía
## Ingesta y Almacenamiento de datos

Almacenamos los datasets en un datalake contruido en AWS con S3 en un bucket público (proyectotres)

los datos tanto mundiales como de colombia están en 

[Datasets](https://github.com/jscaicedom/TETProyecto3/tree/master/Datasets)

Descargamos un archivo más de Colombia tomado de este [link](https://www.datos.gov.co/Salud-y-Protecci-n-Social/Casos-positivos-de-COVID-19-en-Colombia/gt2j-8ykr/data) que no tenía carácteres especiales, 

![Imagen 1](https://github.com/jscaicedom/TETProyecto3/blob/master/Imagenes/Anotaci%C3%B3n%202020-05-14%20185002.jpg)

Creamos un clúster con sus configuraciones
![Cluster](https://github.com/jscaicedom/TETProyecto3/blob/master/Imagenes/Cluster.jpg)

## Procesamiento: Análisis exploratorio de datos con pyspark

Creamos un notebook para el análisis exploratorio de datos con pyspark
![Notebook](https://github.com/jscaicedom/TETProyecto3/blob/master/Imagenes/Jupyter.jpg)

En el notebook de Jupyter hacemos consultas descriptivas exploratorias para conocer el dataset y para comparar los datos de cada uno de los escenarios. Podemos ver las consultas en:

[PROCESAMIENTO](https://github.com/jscaicedom/TETProyecto3/blob/master/Proyecto3.ipynb)

## Visualización básica de datos (Kibana)

Creamos un usuario con 14 días de prueba en elastic.co y un dominio proyecto3
Subimos los datasets a Kibana e hicimos limpieza de datos para corregir errores como datos truncados en la fecha, etc.

![k](https://github.com/jscaicedom/TETProyecto3/blob/master/Imagenes/limpieza.JPG)

Y finalmente hicimos algunas visualizaciones en el dashboard:

[LINK](https://ee62f74110ad477bac661180140117e6.us-east-1.aws.found.io:9243/goto/aad50c97a40a6b3733383df50de0d90d)

En este link se puede ver el dashboard

Usuario: elastic

Contraseña: M6dtvF52cM2rT4akuUuLxpKq


![k](https://github.com/jscaicedom/TETProyecto3/blob/master/Imagenes/Kibana.JPG)

## Visualización básica de datos (EXCEL)

### Situación a nivel mundial

Tomamos los datos de los datasets de las [muertes](https://github.com/jscaicedom/TETProyecto3/blob/master/Datasets/Mundial/time_series_covid19_deaths_global_iso3_regions.csv), [confirmados](https://github.com/jscaicedom/TETProyecto3/blob/master/Datasets/Mundial/time_series_covid19_confirmed_global_iso3_regions.csv) y [recuperados](https://github.com/jscaicedom/TETProyecto3/blob/master/Datasets/Mundial/time_series_covid19_recovered_global_iso3_regions.csv)
los sumamos y pusimos en un nuevo [excel](https://github.com/jscaicedom/TETProyecto3/blob/master/SituacionMundial.xlsx) para graficar los datos:

![situacion mundial](https://github.com/jscaicedom/TETProyecto3/blob/master/Imagenes/smundial.JPG)

### Situación en Colombia

Tomamos los datos del dataset de [Covid en Colombia](https://github.com/jscaicedom/TETProyecto3/blob/master/Datasets/Colombia/Casos_positivos_de_COVID-19_en_Colombia.csv), filtramos los datos por confirmados, recuperados y fallecidos y lo pusimos en un nuevo [Excel](https://github.com/jscaicedom/TETProyecto3/blob/master/Covid%20en%20Colombia.xlsx) para así graficar los datos:

![Situacion en Colombia](https://github.com/jscaicedom/TETProyecto3/blob/master/Imagenes/graficaColombia.jpg)

### Colombia vs Mundo

Tomamos los datos de la [situación mundial](https://github.com/jscaicedom/TETProyecto3/blob/master/SituacionMundial.xlsx) y de la [situación en colombia](https://github.com/jscaicedom/TETProyecto3/blob/master/Covid%20en%20Colombia.xlsx) y los comparamos en un nuevo [excel](https://github.com/jscaicedom/TETProyecto3/blob/master/ColombiaVSMundial.xlsx) para visualizar el vs:

![vs](https://github.com/jscaicedom/TETProyecto3/blob/master/Imagenes/Vs.JPG)
