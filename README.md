# Instalación de Pyspark en Mac Os y Windows 

### En Mac Os
Asegurese de tener JDK(Java Developer Kit) y el XCODE instalado.

Descargamos Apache Spark en [Spark](http://spark.apache.org/downloads.html). Nos situamos en la carpeta de descarga y descomprimimos el tgz.
 ```
 1. tar -xzf spark-2.3.0-bin-hadoop2.7.tgz

 ```
2. Copiamos los el archivo al directorio de aplicaciones adicionales /opt
Nota: en los sistemas linux se instalan aplicaciones opcionales, en mac no esta en automatico, si utiliza homebrew ésta carpeta se creará en automatico.
 
 ```
mv spark-2.3.1-bin-hadoop2.7 /usr/local/opt/spark-2.3.1
 ```
3. Creamos un enlace simbolico a spark(ndica un acceso a un directorio o fichero que se encuentra en un lugar distinto dentro de la estructura de directorios), para tener multiples versiones de Spark.

```
ln -s /usr/local/opt/spark-2.3.1 /usr/local/opt/spark 
```
4. Agregamos al path la ubicación de Spark, esto se deberá hacer en el archivo .bash_profile
```
export PATH="/anaconda3/bin:$PATH"
export SPARK_HOME="/usr/local/opt/spark"

```
5. Finalmente hay que actualizar las variables de entorno del controldor de Spark, para poder correrlo en Jupyter.
```
export PYSPARK_DRIVER_PYTHON="jupyter" 
export PYSPARK_DRIVER_PYTHON_OPTS="notebook" 
export PYSPARK_PYTHON=python3

```

Agregar

```
alias snotebook='$SPARK_HOME/bin/pyspark --master local[2]'

```

Escribimos snotebook en la terminal y se deberia de abri jupyter notebook.



