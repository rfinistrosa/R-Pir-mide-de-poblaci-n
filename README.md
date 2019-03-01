# R-EDA-pirámide de población / despoblación
Análisis exploratorio de datos en R sobre la despoblación en los municipios de España

Hemos creado un dataset a partir de datos públicos extraídos de distintas fuentes institucionales

## FUENTES
Datos | Fuente
------------ | -------------
Municipios | CENTRO DE DESCARGAS DEL CENTRO NACIONAL DE INFORMACIÓN GEOGRÁFICA
Padrón | INE

## DATASET
Una vez realizado el proceso ETL sobre las fuentes, obtenemos el fichero piramide.csv con los siguientes datos:

ID | CAMPO | TIPO | DESCRIPCION
------------ | ------------- | ------------ | -------------
1 | MUNICIPIO | CHAR | Código geográfico y nombre del municipio
2 | COD_INE | CHAR(11) | Código dado por el Instituto Nacional de Estadística a cada una de las entidades poblacionales. Se caracteriza por ser un código único e intransferible formado por 11 dígitos de los cuales los dos primeros hacen referencia a la provincia a la que pertenece la unidad poblacional. Los tres siguientes identifican el número del municipio dentro de la provincia. Los dos siguientes indican si es o no entidad colectiva. Los dos siguientes indican si la población es un núcleo poblacional o es indican si es entidad singular. Y los dos finales población diseminada por el término municipal.
3 | SEXO | CHAR(1) | T = TODOS (suma de H y M), H = Hombres, M = Mujeres
4 | TOTAL_EDAD | DOUBLE | Número total de habitantes
5 | 0 | NUMERO | Número de habitantes de 0 años
6 | 1 | NUMERO | Número de habitantes de 1 año
n | n | NUMERO | Número de habitantes de n años
104 | 99 | NUMERO | Número de habitantes de 99 años
105 | 100 | NUMERO | Número de habitantes de más de 100 años
106 | EDAD_MEDIA | DOUBLE | Edad media del municipio
107 | de0-18 | INTEGER | Número de habitantes menores de 18 años
108 | de19-67 | INTEGER | Número de habitantes entre 19 y 67 años
109 | masde68 | INTEGER | Número de habitantes mayores de 18 años
110 | de0-12 | INTEGER | Número de habitantes entre 0 y 12 años
111 | DENSIDAD | DOUBLE | Edad media del municipio
112 | DESPOBLACION | INTEGER | 0 = Densidad >= 12.5, 1 = Densidad < 12.5

## EDA
Utilizando R y sus librerías de representación geoespacial, demostramos cómo realizar un análisis exploratorio de datos (EDA)

Las librerías R que se utilizan en éste ejercicio son:

* ggplot2 - Librería para análisis exploratorio de datos
* plotrix - Librería para análisis exploratorio de datos

