# Instalación de Pyspark en Mac Os y Windows 

### En Mac Os
Descargamos Apache Spark en [Spark](http://spark.apache.org/downloads.html). Nos situamos en la carpeta de descarga y descomprimimos el tgz.
 ```
 1. tar -xzf spark-2.3.0-bin-hadoop2.7.tgz

 ```
2. Copiamos los el archivo al directorio de aplicaciones adicionales /opt
 
 ```
mv spark-2.3.1-bin-hadoop2.7 /usr/local/opt/spark-2.3.1
 ```
3. Creamos un enlace simbolico a spark(ndica un acceso a un directorio o fichero que se encuentra en un lugar distinto dentro de la estructura de directorios), para tener multiples versiones de Spark.

```
ln -s /usr/local/opt/spark-2.3.1 /usr/local/opt/spark 
```
4. Agregamos al path la ubicación de Spark
```
export PATH="/anaconda3/bin:$PATH"
export PATH="/anaconda3/bin:$PATH"
export SPARK_HOME="/usr/local/opt/spark"

```
5. Finalmente hay que actualizar las variables de entorno del controldor de Spark, para poder correrlo en Jupyter.
```
export PYSPARK_DRIVER_PYTHON="jupyter" 
export PYSPARK_DRIVER_PYTHON_OPTS="notebook" 
```

Agregar

```
alias snotebook='$SPARK_HOME/bin/pyspark --master local[2]'

```
Escribimos snotebook en la terminal y se deberia de abri jupyter notebook.


### En windows
Descargamos Apache Spark en [Spark](http://spark.apache.org/downloads.html), seleccionamos la versión y descargamos el archivo tgz. Descomprimimos. 

Abrimos simbolo de sistema y pegamos las siguientes instrucciones
```
setx SPARK_HOME C:\spark-2.3.2

setx PYSPARK_DRIVER_PYTHON ipython

setx PYSPARK_DRIVER_PYTHON_OPTS notebook
```
Les debera aparecer la salida.
correcto se guardo el valor especificado.

Ahora debemos poner C:\spark-2.3.2\bin en el path, para ello nos vamos a "Editar la variables del sistema->" "variables de entorno" seleccionamos path y le damos Editar, presionamos nuevo y agregagos C:\spark-2.3.2\bin. 
