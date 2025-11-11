# Laboratorio de Comunicaciones
## Universidad Industrial de Santander

---
# Misión 6: Nuestra Propia Emisora FM Estéreo

### Integrantes
- **MICHELLE GARZÓN CAMPOS** - 2202785
- **JOHAN SEBASTIAN FANDIÑO** - 2204271

Escuela de Ingenierías Eléctrica, Electrónica y de Telecomunicaciones  
Universidad Industrial de Santander

---

## Declaración de Originalidad y Responsabilidad
Los autores de este informe certifican que el contenido aquí presentado es original y ha sido elaborado de manera independiente. Se han utilizado fuentes externas únicamente como referencia y han sido debidamente citadas.

Asimismo, los autores asumen plena responsabilidad por la información contenida en este documento. 

Uso de IA: Se utilizó ChatGPT para reformular secciones del texto y verificar gramática, pero el contenido técnico fue desarrollado íntegramente por los autores.

---
## Contenido

### Resumen.
En esta práctica la misión es crear nuestra propia emisora, esto se logrará mediante la creación de un pequeño bloque de programación para ser transmitido en el campus universitario, que pueda ser sintonizado por cualquier receptor de radio FM estándar. Para esto se utilizó la IA y el software Audacity para crear un archivo de audio el cual haría la interpretación del locutor de la emisora, se combina este audio con una canción llamativa y se mazteriza para asegurar que sea un archivo estéreo. El archivo de audio resultante es el que se transmitirá mediante el USRP para poder ser percibido por dispositivos cuya antena capte señales FM.

**Palabras clave:** Emisora FM, Aucio estéreo, USRP, GNU Radio.

### Introducción.
En esta misión el propósito es crear un archivo de audio estéreo el cual deberá ser percibido por dispositivos con antenas capaces de captar señales FM, Esto es lo que llamaremos como "nuestra propia emisora FM". Para la construcción de este archivo de audio y su correcta transmisión se dividió la práctica en las siguientes fases:
  1) Fase inicial.
  2) Fase crítica.
  3) Fase final.

### Fase 1.
En esta fase se utilizó la IA para para darle cuerpo al mensaje que se creó en conjunto con el grupo de trabajo, utilizando una voz llamativa que le diera un tono de locutora de radio e hiciera sonar interesante e interactivo el mensaje. Luego se uso el software de edición de audio Audacity en donde se masterizó y mezcló el audio creado con la IA en conjunto con una canción llamativa del momento para obtener un archivo de audio estéreo resultante muy llamativo y con un estilo a emisora ordinaria agregandole ese toque de actualidad con la canción elegida. Este archivo de audio resultante debía durar de 60 a 90 segundos y será el que se transmitirá para probar y evaluar la eficiencia de "nuestra propia emisora FM". 


### Fase 2. 
Con el audio resultante finalizado se pasó a la fase crítica en la que mediante el software GNU Radio se procesó la señal para darle la estructura que deseabamos. Para esto lo primero que se hizo fue cargar el archivo de audio .wav y separar sus componentes estéreo L y R. Con esto se creó la señal de suma L+R para compatibilidad monofónica la cual iba hasta los 15KHz, el tono piloto de 19 kHz que es la referencia de fase para la demodulación estéreo y la señal L-R, esta última se moduló en una subportadora de 38 kHz mediante AM de Doble Banda Lateral con Portadora Suprimida. Finalmente se sumaron las 3 señales mencionadas anteriormente para formar la señal resultante MPX, esta señal MPX es la que será transmitida en el laboratorio y la que será la prueba 01 de "nuestra propia emisora FM". Para asegurar de que la señal MPX tiene la estructura deseada se revisó el espectro en frecuencia de esta señal y para verificar la correcta ubicación y amplitud relativa de cada uno de sus componentes. El espectro en frecuencia obtenido de la señal MPX es el siguiente:

imagen.................

### Fase 3.
Una vez ralizados los pasos anteriores pasamos a la fase final de la misión, en esta fase el propósito es llevar a la señal MPX al dominio de radiofrecuencia para su emisión y se comprueba su correcta recepción. Para lograr esto lo primero que se hizo fué añadir el bloque de modulación FM y configurarlo de modo que la señal MPX generada sea la entrada a este bloque y se ajustó la desviación de frecuencia para cumplir con el estándar de radiodifusión de 75KHz, luego se modificaron los parámetros de transmision del bloque USRP como la ganancia y la tasa de muestreo para obtener una señal limpia en el receptor, igualmente de acuerdo con los registros oficiales acerca de radiodifusión de la ANE se decició con el equipo de trabajo establecer la señal MPX en 107MHz como frecuencia central de transmisión

### Análisis y Conclusiones

---

Volver al [INICIO](#laboratorio-de-comunicaciones)
