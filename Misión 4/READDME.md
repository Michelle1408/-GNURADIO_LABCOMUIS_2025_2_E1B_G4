# Práctica 4: VIGILANCIA DEL ESPECTRO LEGAL

### Integrantes
- **MICHELLE GARZÓN CAMPOS - 2202785**
- **JOHAN SEBASTIAN FANDIÑO RUIZ - 2204271**

Escuela de Ingenierías Eléctrica, Electrónica y de Telecomunicaciones  
Universidad Industrial de Santander

---

## Declaración de Originalidad y Responsabilidad
Los autores de este informe certifican que el contenido aquí presentado es original y ha sido elaborado de manera independiente. Se han utilizado fuentes externas únicamente como referencia y han sido debidamente citadas.

Asimismo, los autores asumen plena responsabilidad por la información contenida en este documento. 

Uso de IA: [Indicar si se usó IA y para qué aspectos específicos, por ejemplo: "Se utilizó ChatGPT para reformular secciones del texto y verificar gramática, pero el contenido técnico fue desarrollado íntegramente por los autores."]

---
## Contenido

### Resumen
Para esta práctica numero 4 se busca realizar una auditoría del espectro FM para verificar que todas las transmisiones activas en el área metropolitana de bucaramanga operen con una licencia válida y en sus parámetros autorizados, identificando cualquier posible transmisión "ilegal". Para esto se plantearon 3 fases que pretenden cumplir con el objetivo. 

**Palabras clave:** espectro FM, radiodifusión,MinTIC, Coincidencia legal. 

### Introducción
En la práctica 4 el objetivo principal es auditar el espectro de radiodifusión sonora en Frecuencia Modulada (FM) de Bucaramanga, comparando las señales detectadas en campo con los registros oficiales del MinTIC y la ANE para identificar transmisiones no autorizadas y verificar que las frecuencias registradas operen en los parámetros asignados.para esto primero se hizo un filtrado de los registros oficiales del ANE para centrarnos en los registros en el área metropolitana de bucaramanga, para posterior mente hacer un barrido en frecuencia con ayuda del SDR y el software GNU Radio y verificar la información del paso anterior, y por último se hace una comparación de lo observado en el laboratorio y los registros del ANE.


### Fase 1: Inteligencia y Preparación (Investigación Regulatoria)
En la fase 1 se realizó como primer paso la busqueda de datos oficiales registrados por el MinTIC sobre estaciones de radiodifusión sonora en FM, luego se filtró esta información para obtener las estaciones de radiodifusión en la zona de interes la cual era el área metropolitanda de bucaramanga, se hizo un registro de estas estaciones destacando información característica como Frecuencia Asignada, Distintivo de Llamada, Nombre Comercial de la Emisora y Clase de emisora. Esta información fué registrada en la siguiente tabla:
<img src="Captura de pantalla 2025-10-08 102623.png" width="1000">
esta informacón sera nuestro punto oficial de comparación con el que contrastaremos los resultados obtenidos en el desarrollo de esta práctica.

### Fase 2: Monitoreo de Campo (Escaneo del Espectro)
Para la fase 2 el objetivo es hacer una inspección a los datos de la tabla anterior, para esto se utilizó el equipo SDR junto con una antena para percibir las señales de radiodifusión sonora en FM, y el sotfware GNU Radio para poder observar las características del espectro en frecuencia. Con los dipositivos enlazados y configurados se procedió a hacer un barrido completo de la banda de FM, desde los 88.0 MHz hasta 108.0 MHz. En este barrido se hizo un nuevo registro de las señales percibidas por la antena en el que se anotaron la potencia, frecuencia exacta en la que sencontró y ancho de banda de la señal emisora en cuectión. los resultados obtenidos se comprararon con los datos oficiales del MinTIC para hacer veeduria de que las emisoras registradas en la tabla anterior operaran en las condiciones especificadas en esta misma tabla. esta comparación se puede observar en la siguiente tabla:
<img src="imagenes/Captura de pantalla 2025-10-08 074646.png" width="1000">


### Conclusiones
Se sintetizan los principales aportes y puntos relevantes de la práctica, evitando repetir lo ya consignado en las otras secciones del informe. 

### Referencias
Ejemplo de referencia:

- [Proakis, 2014] J. Proakis, M. Salehi. Fundamentals of communication systems. 2 ed. England: Pearson Education Limited, 2014. p. 164-165, 346. Chapter 5 In: [Biblioteca UIS](https://uis.primo.exlibrisgroup.com/permalink/57UIDS_INST/63p0of/cdi_askewsholts_vlebooks_9781292015699)

