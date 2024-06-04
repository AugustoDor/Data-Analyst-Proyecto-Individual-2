# Proyecto Individual n°2
# Data Analyst

### Contexto
Los siniestros viales son eventos que involucran vehículos en las vías públicas, los cuales pueden tener diversas causas como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos, o incluso caídas de vehículos. Estos incidentes pueden tener consecuencias que van desde daños materiales hasta lesiones graves o fatales para los involucrados.

Las tasas de mortalidad relacionadas con siniestros viales son un indicador crítico de la seguridad vial en una región. Estas tasas se calculan, generalmente, como el número de muertes por cada cierto número de habitantes, o por cada cierta cantidad de vehículos registrados.

En Argentina, cada año mueren cerca de 4.000 personas en siniestros viales. Aunque muchas jurisdicciones han logrado disminuir la cantidad de accidentes de tránsito, estos sigue siendo la principal causa de muertes violentas en el país.


### El Proyecto
El Observatorio de Movilidad y Seguridad Vial (OMSV), del Gobierno de la Ciudad Autónoma de Buenos Aires, nos solicita la elaboración de un proyecto de "análisis de datos", con el fin de generar información que le permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales. Para tal fin, nos dejan a disposición un dataset que contiene información sobre los siniestros viales registrados en la Ciudad de Buenos Aires durante el periodo 2016-2021.


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

## III. Elaboración de panel de instrumentos (dashboard)

El archivo que controla el panel de instrumentos fue elaborado en Power BI.