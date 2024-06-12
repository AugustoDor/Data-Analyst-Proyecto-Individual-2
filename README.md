<h1 align='center'>
 <b>PROYECTO INDIVIDUAL Nº2</b>
</h1>

# <h1 align="center">**`Siniestros viales`**</h1>

<p align='center'>
<img src = 'https://static.lajornadaestadodemexico.com/wp-content/uploads/2022/08/Siniestros-viales.jpg' height = 500>
<p>

## **Descripción del problema -contexto y rol a desarrollar-**

Los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, son eventos que involucran vehículos en las vías públicas y que pueden tener diversas causas, como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos o caídas de vehículos. Estos incidentes pueden tener consecuencias que van desde daños materiales hasta lesiones graves o fatales para los involucrados.

En el contexto de una ciudad como Buenos Aires, los siniestros viales pueden ser una preocupación importante debido al alto volumen de tráfico y la densidad poblacional. Estos incidentes pueden tener un impacto significativo en la seguridad de los residentes y visitantes de la ciudad, así como en la infraestructura vial y los servicios de emergencia.

Las tasas de mortalidad relacionadas con siniestros viales suelen ser un indicador crítico de la seguridad vial en una región. Estas tasas se calculan, generalmente, como el número de muertes por cada cierto número de habitantes o por cada cierta cantidad de vehículos registrados. Reducir estas tasas es un objetivo clave para mejorar la seguridad vial y proteger la vida de las personas en la ciudad.

Es importante destacar que la prevención de siniestros viales involucra medidas como la educación vial, el cumplimiento de las normas de tráfico, la infraestructura segura de carreteras y calles, así como la promoción de vehículos más seguros. El seguimiento de las estadísticas y la implementación de políticas efectivas son esenciales para abordar este problema de manera adecuada.


### **Contexto**

En Argentina, cada año mueren cerca de 4.000 personas en siniestros viales. Aunque muchas jurisdicciones han logrado disminuir la cantidad de accidentes de tránsito, esta sigue siendo la principal causa de muertes violentas en el país.
Los informes del Sistema Nacional de Información Criminal (SNIC), del Ministerio de Seguridad de la Nación, revelan que entre 2018 y 2022 se registraron 19.630 muertes en siniestros viales en todo el país. Estas cifras equivalen a 11 personas por día que resultaron víctimas fatales por accidentes de tránsito.

Solo en 2022, se contabilizaron 3.828 muertes fatales en este tipo de hechos. Los expertos en la materia indican que en Argentina es dos o tres veces más alta la probabilidad de que una persona muera en un siniestro vial que en un hecho de inseguridad delictiva.

### **Rol a desarrollar**

El `Observatorio de Movilidad y Seguridad Vial` (OMSV), centro de estudios que se encuentra bajo la órbita de la ***Secretaría de Transporte*** del Gobierno de la Ciudad Autónoma de Buenos Aires, nos solicita la elaboración de un proyecto de anális de datos, con el fin de generar información que le permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales.
Para ello, nos disponibilizan un dataset sobre homicidios en siniestros viales acaecidos en la Ciudad de Buenos Aires durante el periodo 2016-2021. Este dataset se encuentra en formato *xlsx* y contiene dos hojas llamadas: **hechos** y **víctimas**. Asimismo, observarán que incluye otras dos hojas adicionales de diccionarios de datos, que les podrá servir de guía para un mayor entendimiento de la data compartida.

Por su parte, en la sección **Material de apoyo** podrán encontrar más información de interés relativa a los datos disponibilizados y al Observatorio que nos encomienda el trabajo.

### Objetivos
- A. Llevar a cabo un análisis básico de ETL

- B. Desarrollar un análisis EDA

- C. Desarrollar un tablero de visualización (dashboard) que contenga los hallazgos, el desarrollo de los KPIs propuestos.

- D. Llevar a cabo una presentación, de máximo 10 mins, con la información relevante del desarrollo del proyecto 

---> KPIs propuestos:

Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.

Definimos a la tasa de homicidios en siniestros viales como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. Su fórmula es: (Número de homicidios en siniestros viales / Población total) * 100,000.

Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.

Definimos a la cantidad de accidentes mortales de motociclistas en siniestros viales como el número absoluto de accidentes fatales en los que estuvieron involucradas víctimas que viajaban en moto en un determinado periodo temporal. Su fórmula para medir la evolución de los accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en moto en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100. 

# ETAPAS DEL PROYECTO

## I. ETL (Extraction, Transformation and Load)

Fue considerado un (1) archivo, en formato excel, como fuente primaria de información:
- homicidios.xlsx
Este archivo, contaba con 2 tablas:

**Tabla HECHOS:**
* Tratamiento de filas completas que solo contienen valores 'Null'
* Ajuste del formato y tipo de las columnas
* Cambiar nombre de columnas

**Tabla VICTIMAS:**
* Tratamiento de filas completas que solo contienen valores 'Null'
* Ajuste del formato y tipo de las columnas
* Cambiar nombre de columnas

Una vez finalizado este proceso fueron guardados con formato parquet y csv.

## II. EDA (Exploration Data Analysis)

Para el EDA se genera una archivo combinado de los 2 archivos anteriormente transformados.
Este archivo combinado es utilizado para iniciar el estudio EDA, teniendo como `objetivo específico encontrar "correlaciones efectivas" entre las variables de interés para el estudio`.

**1. Visualización de Datos Geoespaciales** ---> visualizar en un mapa los siniestros viales registrados en los archivos fuentes.

**2. Ejercicio de filtración para aprovechamientode variables de interés**

**3. Tratamiento de Variables de interés**
* 3.1 Tratamiento de valores pérdidos | nulos | vacíos | duplicados

* 3.2 Tratamiento de valores atípicos (outliers)

* 3.3 Visualización de variables categóricas. Ver

* 3.4 Visualización Histográfica

* 3.5 Matriz de Correlaciones


**4. Conclusiones EDA - Correlaciones**

* **Sobre información inválida o pérdida (missing):**
Únicamente fueron encontrados errores simples en datos aislados de las variables de interés: 'hora', 'latitud' y 'longitud'. Todos superados sin incidencia alguna en el análisis EDA.

* **Sobre información de los datos atípicos (Outliers):**  
En las columnas; 'latitud' y 'longitud' fueron evidenciados datos atípicos, no obstante su existencia es explicable razonablemente. Para el tema de las localizaciones geoespaciales (latitud, longitud), los datos atípicos hacen relación al valor cero '0' que les fue asignado a aquellos campos en ausencia de algún valor en los datos del dataset original, representando apenas un 1.81% de la muestra para dichas variables.

* **Sobre la información de potenciales correlaciones entre las variables:**
Al respecto el ejercicio nos muestra evidencia de una fuerte relación, de '0.81' entre las variables; 'rol' y 'vehiculo_victima', reflejando la importancia que tienen tanto el vehículo de movilización, como la posición que ocupa la víctima en dicho vehículo. Esas variables, a su vez parecen mostrar algunas correlaciones, aunque muy moderada, con las edades de las víctimas ('0.42' y '0.36' respectivamente). De igual forma, la variable 'fecha' (Año del siniestro) muestra una correlación de baja intensidad con la variable 'lugar' ('0.29'), en tanto que la variable 'hora' (Hora del siniestro) tiene una relación moderada baja ('0.24') con el tipo de vehículo en el que se transporta la víctima siniestrada. Por último se evidencia una correlación baja, del '0.31' entre el lugar del siniestro (Dirección donde ocurrió el siniestro) y el tipo de vía de tránsito (Avenidas, Calles, Autopistas o Avenida General Paz).

<br />

## III. Elaboración de panel de instrumentos (dashboard)

El archivo que controla el panel de instrumentos fue elaborado en Power BI.
