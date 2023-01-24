
# TP-topicos-avanzados
### repositorio de trabajo de Natalia Debandi
nataliadebandi@gmail.com
Este repositorio fue desarrollado en base al que se presentó en el Seminario de Topicos Avanzados (ITBA)

https://github.com/arjones/bigdata-workshop-es

## Contenidos
Se presenta exclusivamente lo vinculado con el Trabajo Practico y los ajustes. 

El repositorio se mantuvo con la misma configuración que el original (ver infraestructura) y para mayor información se puede consultar en:
https://github.com/arjones/bigdata-workshop-es

### Dataset

covid/

en esa carpeta se encuentran los 3 archivos:
covid19casos.csv
migrantes2020.csv
migrantes2021.csv

Como son muy pesados para subirse al GITHUB se pueden acceder en este enlace:
https://drive.google.com/open?id=1vrCW3zm0vIvJjOu_hGg8myCjWKYqxoAG&authuser=nataliadebandi%40gmail.com&usp=drive_fs

parquetv4/
Aqui se almacenan dos instancias intermedias dentro del procesamiento:

covidmigrantes.parquet

Es producto del procesamiento realizado en el notebook jupyter/notebook//TPDebandi/preprocesamiento.ipynb

covidclasif2.parquet

Este archivo de parquet se almacena luego de la creación de features para poder retomar el análisis sin tener que correr todo.


### Análisis

La notebook de análisis de los datos está en
jupyter/notebook/TPDebandi/analisis-covid.ipynb

Esta notebook lee directamente el archivo parquet que se construyeó en:
jupyter/notebook//TPDebandi/preprocesamiento.ipynb

El objetivo del análisis es lograr predecir a partir de un conjunto de variables (sexo, género, tiempo entre diagnostico y tratamiento,nacionalidad,semana epidemiológica, tipo de financiamiento en la atención médica) el fallecimiento o no de una persona por COVID.
Es importante aclarar que se trata de un ejercicio y que si bien los datos son reales no se pretende efectivamente realizar una clasificación de esta índole, ya que consideramos que no tiene mucho sentido. Se requieren de variables vinculadas a las condiciones previas del paciente y epidemilógicas.


## Infrastructura

El workshop simula una instalación de producción utilizando container de Docker.
[docker-compose.yml](docker-compose.yml) contiene las definiciones y configuraciones para esos servicios y sus respectivas UIs:

* Apache Spark: [Spark Master UI](http://localhost:8080) | [Job Progress](http://localhost:4040)
* Apache Kafka:
* Postgres:
* [Superset](http://superset.incubator.apache.org): [Nuestro Dashboard](http://localhost:8088/)

Los puertos de acceso a cada servicio quedaron los defaults. Ej: **spark master:7077**, **postgres: 5432**





## entorno creado por:
Gustavo Arjones &copy; 2017-2020
[arjon.es](https://arjon.es) | [LinkedIn](http://linkedin.com/in/arjones/) | [Twitter](https://twitter.com/arjones)

Mutt Data &copy; 2021-
