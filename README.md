# Accidentalidad en medellin

## Introduccion

El presente trabajo buscara predecir la accidentalidad de medellin entre los años 2021 a 2022, para esto se construira un modelo de prediccion con el cual se entrenara con los años 2014 a 2018, y se validaron desde 2019 a 2020.

## Analisis Exploratorio
Lo primero que haremos sera manipular la variable de FECHA_ACCIDENTE, con el fin de extraer informacion que solo nos de como resultado la fecha con el año,mes y dia.

Para la ingenieria de caracteristicas crearemos una nueva variable llamada 'Festivos', para esto crearemos una serie de condiciones a modo de lista en la cual relacionandola con la variable FECHA_ACCIDENTE, para que cada vez que una fecha que es considerada festiva sea encontrada , entonces el programa asignara a 'Festivos' un valor de Si, al terminar , los valores restantes seran considerados nulos y por ende a esos nulos se les asigna un valor de No.


![](https://github.com/Efbarrientosa/Trabajo-3-TAE/blob/main/01.PNG)

Lo siguiente sera manipular valores erroneos en variables de gravedad de accidentes , comunas , eliminando columnas que son poco informativas o transformando valores que son redundantes con otros.Ademas se crean variables de SEMANA y DIA_DE_LA_SEMANA usando funciones de formato DATE.


![](https://github.com/Efbarrientosa/Trabajo-3-TAE/blob/main/02.PNG)

### Clase de Accidente y dia de la semana
Como podemos ver en la siguiente grafica vemos que hay una mayor cantidad de accidentes los dias viernes, lo cual es normal ya que es un dia en que la gente tiende a descuidarse, ademas como podemos ver , el tipo de accidente siempre es choque,mientras que el menor que es casi omitible siempre son incendios.

Imagen03
![](https://github.com/Efbarrientosa/Trabajo-3-TAE/blob/main/03.png)

### Festivos
Como es normal , si un dia es festivo o no, no es un indicativo suficiente , ya que los festivos son pocos en comparacion con los dias que no son festivos.


![](https://github.com/Efbarrientosa/Trabajo-3-TAE/blob/main/04.png)
### Comunas
Aqui podemos ver la cantidad de accidentes  que ocurren en cada comuna , como podemos ver el sector de la calendaria es la comuna con mas cantidad de accidentes , lo cual  es logico ya que se ubica en una zona muy concurrida como el centro de la ciudad.


![](https://github.com/Efbarrientosa/Trabajo-3-TAE/blob/main/05.png)
### Gravedad del Accidente y Año
Como podemos ver el año 2016 es uno de los años con mas accidentalidad , ademas de que la gravedad del accidente tiende a ser con mas heridos , como informacion adicional tenemos que el año 2020 y 2014 no tienen sus registros completos por lo cual la informacion es menor que en otros años.


![](https://github.com/Efbarrientosa/Trabajo-3-TAE/blob/main/06.png)
## Agrupamiento
Para esto usaremos los archivos que proporciona el sistema de informacion geografica de medellin , intentaremos crear un agrupammiento , para esto usaremos el metodo del codo para que nos indique un k adecuado para el metodo de agrupamiento k-medias


![](https://github.com/Efbarrientosa/Trabajo-3-TAE/blob/main/07.png)

Una vez realizado el clustering, analizamos los grupos y los graficamos , algunos barrios no pueden ser mostrados por las transformaciones en los datos anteriores.

Al analizar las bondades de los grupos nos damos cuenta que el grupo 1 y 2 cuentan con mayor accidentalidad , mientras que los grupos 3 y 4 cuentan con menos accidentalidad.




![](https://github.com/Efbarrientosa/Trabajo-3-TAE/blob/main/08.PNG)

##Referencias
[StackOverflow](https://stackoverflow.com/)
[MEDATA](http://medata.gov.co/dataset/incidentes-viales)
[GeoMedellin](https://geomedellin-m-medellin.opendata.arcgis.com/datasets/limite-barrio-vereda-catastral/explore?location=6.268865%2C-75.595576%2C12.61)
