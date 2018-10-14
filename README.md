# Instalación de Pyspark en Mac Os y Windows 

Abrimos simbolo de sistema y pegamos las siguientes instrucciones
```
setx SPARK_HOME C:\spark-2.3.2

setx HADOOP_HOME C:\spark-2.3.2

setx PYSPARK_DRIVER_PYTHON ipython

setx PYSPARK_DRIVER_PYTHON_OPTS notebook

```
Les debera aparecer la salida.
correcto se guardo el valor especificado.

Ahora debemos poner C:\spark-2.3.2\bin en el path, para ello nos vamos a "Editar la variables del sistema->" "variables de entorno" seleccionamos path y le damos Editar, presionamos nuevo y agregagos C:\spark-2.3.2\bin. 
