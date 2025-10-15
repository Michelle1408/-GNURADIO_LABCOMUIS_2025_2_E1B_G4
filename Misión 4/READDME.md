# Práctica 4: VIGILANCIA DEL ESPECTRO LEGAL

### Integrantes
- **MICHELLE GARZÓN CAMPOS - 2202785**
- **JOHAN SEBASTIAN FANDIÑO RUIZ - 2204271**

Escuela de Ingenierías Eléctrica, Electrónica y de Telecomunicaciones  
Universidad Industrial de Santander

---

## Declaración de Originalidad y Responsabilidad.
Los autores de este informe certifican que el contenido aquí presentado es original y ha sido elaborado de manera independiente. Se han utilizado fuentes externas únicamente como referencia y han sido debidamente citadas.

Asimismo, los autores asumen plena responsabilidad por la información contenida en este documento. 

Uso de IA: [Indicar si se usó IA y para qué aspectos específicos, por ejemplo: "Se utilizó ChatGPT para reformular secciones del texto y verificar gramática, pero el contenido técnico fue desarrollado íntegramente por los autores."]

---
## Contenido.

### Resumen.
Para esta práctica numero 4 se busca realizar una auditoría del espectro FM para verificar que todas las transmisiones activas en el área metropolitana de bucaramanga operen con una licencia válida y en sus parámetros autorizados, identificando cualquier posible transmisión "ilegal". Para esto se plantearon 3 fases que pretenden cumplir con el objetivo. 

**Palabras clave:** espectro FM, radiodifusión,MinTIC, Coincidencia legal. 

### Introducción.
En la práctica 4 el objetivo principal es auditar el espectro de radiodifusión sonora en Frecuencia Modulada (FM) de Bucaramanga, comparando las señales detectadas en campo con los registros oficiales del MinTIC y la ANE para identificar transmisiones no autorizadas y verificar que las frecuencias registradas operen en los parámetros asignados.para esto primero se hizo un filtrado de los registros oficiales del ANE para centrarnos en los registros en el área metropolitana de bucaramanga, para posterior mente hacer un barrido en frecuencia con ayuda del SDR y el software GNU Radio y verificar la información del paso anterior, y por último se hace una comparación de lo observado en el laboratorio y los registros del ANE.


### Fase 1: Inteligencia y Preparación (Investigación Regulatoria).
En la fase 1 se realizó como primer paso la busqueda de datos oficiales registrados por el MinTIC sobre estaciones de radiodifusión sonora en FM, luego se filtró esta información para obtener las estaciones de radiodifusión en la zona de interes la cual era el área metropolitanda de bucaramanga, se hizo un registro de estas estaciones destacando información característica como Frecuencia Asignada, Distintivo de Llamada, Nombre Comercial de la Emisora y Clase de emisora. Esta información fué registrada en la siguiente tabla:
<img src="imagenes/Captura de pantalla 2025-10-08 102623.png" width="1000">
esta informacón sera nuestro punto oficial de comparación con el que contrastaremos los resultados obtenidos en el desarrollo de esta práctica.

### Fase 2: Monitoreo de Campo (Escaneo del Espectro).
Para la fase 2 el objetivo es hacer una inspección a los datos de la tabla anterior, para esto se utilizó el equipo SDR junto con una antena para percibir las señales de radiodifusión sonora en FM, y el sotfware GNU Radio para poder observar las características del espectro en frecuencia. Con los dipositivos enlazados y configurados se procedió a hacer un barrido completo de la banda de FM, desde los 88.0 MHz hasta 108.0 MHz. En este barrido se hizo un nuevo registro de las señales percibidas por la antena en el que se anotaron la potencia, frecuencia exacta en la que se encontró y ancho de banda de la señal emisora en cuestión. los resultados obtenidos se comparararon con los datos oficiales del MinTIC para hacer veeduria de que las emisoras registradas en la tabla anterior operaran en las condiciones especificadas en esta misma tabla. esta comparación se puede observar en la siguiente tabla:
<img src="imagenes/Captura de pantalla 2025-10-08 074646.png" width="1000">
En esta tabla se puede observar un registro para la frecuencia en la que debería operar cada emisora FM segun registros del MinTIC y un registro de la frecuencia en la que se encontró cada emisora FM en la práctica de laboratorio, además se hizo el registro de las características mencionadas anteriormente para cada señal. durante el barrido hubo emisoras cuya señal no fué posible detectar, de manera que no se pudo hacer un registro de frecuncia, potencia y ancho de banda, para estas emisoras se les asigno una casilla de color rojo en los parámetros mencionados.

### Fase 3: Análisis y Cruce de Datos.
Para esta fase se plantea finalizar la práctica con el cumplimiento del objetivo de esta misma. Para esto se hace una clasificación de las emisoras encontradas en el barrido. si las características de la señal coinciden con los datos oficiales del MinTIC se asigna como Coincidencia Legal. Por el contrario si las caracteristicas de la señal difieren con los datos oficiales del MinTIC se asigna como Posible Desviación. los resultados de esta clasificación se pueden apreciar en la siguiente tabla:
<img src="imagenes/Captura de pantalla 2025-10-08 074705.png" width="1000">

### Resultados y hallazgos.
Durante la práctica se pudo formar la creación de una tabla maestra que compara los resultados obtenidos en la misión con los datos oficiales y una imagen panorámica en la que se identifican algunas de las emisoras de los documentos oficiales. A continuación la tabla y la imagen panorámica:
<img src="imagenes/Captura de pantalla 2025-10-08 074705.png" width="1000">
<img src="imagenes/Imagen de WhatsApp 2025-09-17 a las 16.54.41_b24ddf91.jpg" width="1000">
Se pueden apreciar en esta panorámica 5 picos notables por encima del ruido, estos picos luego de un análisis de frecuencia y comparación de datos, encontramos de donde provenían, el primero pertenece a la W Radio (90.7MHz), el segundo pertenece a la Policía Nacional de Bucaramanga (91.7 MHz), el tercero es la señal emitida por la radio FM Radionica (92.3 MHz), el cuarto pico que se observa es por la radio FM Colombia estéreo cuya frecuencia es 92.9 MHz, y el ultimo pertenece a la Emisora Comunitaria la Brújula- Área de ServicioNo.1 (90.4MHz).
Con este análisis se encontraron también 2 señales que clasificamos como posibles transmisiones no identificadas, estas fueron la de UIS ESTEREO BUCARAMANGA que se ubicó a los 96.9MHz(imagen1 y 3), y LA EXITOSA que se ubicó a 98.5 MHz, a continuación el espectro de cada una de estas:
<img src="imagenes/Imagen de WhatsApp 2025-09-17 a las 17.31.52_c3644635.jpg" width="450">
<img src="imagenes/Imagen de WhatsApp 2025-09-17 a las 17.37.01_c4e087ab.jpg" width="450">
Una posible razón por la que aparecen emisoras que no están en la lista oficial es que podrían estar transmitiendo sin autorización, es decir, funcionan como emisoras “piratas” que no cuentan con licencia del MinTIC o la ANE, lo cual suele pasar en algunas ciudades del país. Otra explicación es que esas frecuencias sí tienen licencia, pero en municipios cercanos, y la señal alcanza a llegar a Bucaramanga
gracias a la potencia de transmisión y a las condiciones del terreno. A continuación una imagen del espectro en frecuencia para cada posible transmisión no identificada, tomada desde elanalizador de espectros.
<img src="imagenes/Imagen de WhatsApp 2025-09-22 a las 22.30.04_6dca3a16.jpg" width="450">
<img src="imagenes/Imagen de WhatsApp 2025-09-22 a las 22.30.04_e1a6560a.jpg" width="450">
Durante el barrido del espectro una de las principales dificultades fue identificar con claridad algunas emisoras, ya que varias señales se encontraban muy cercanas en frecuencia y resultaba complicado diferenciarlas. También se presentaron señales débiles que apenas se destacaban sobre el ruido de fondo, lo que hizo más difícil su reconocimiento. Además, el nivel de ruido en ciertos tramos de la banda
afectó la calidad de la visualización en el espectro, generando dudas sobre si se trataba de emisoras reales o simples interferencias.


### Conclusiones
En el barrido realizado sobre la banda de FM en Bucaramanga se encontraron coincidencias con la mayoría de emisoras registradas oficialmente, lo cual refleja un uso en general ordenado del espectro. Sin embargo, se detectaron dos señales que no aparecen en la lista oficial: UIS Estéreo (96.9 MHz) y La Exitosa (98.5 MHz). Estas transmisiones representan anomalías que deben revisarse, ya que pueden corresponder a emisoras sin licencia o a coberturas provenientes de municipios cercanos.
Como inspector de la ANE, recomendaría realizar una verificación en sitio para ambas frecuencias con equipos certificados, con el fin de confirmar si operan dentro de los parámetros legales establecidos en el Plan Técnico Nacional de Radiodifusión Sonora FM. En caso de comprobarse que son emisoras no autorizadas, se deberían iniciar los procesos sancionatorios correspondientes; si se trata de coberturas legítimas, actualizar la información en los registros para reflejar mejor la situación real del espectro en la región.



