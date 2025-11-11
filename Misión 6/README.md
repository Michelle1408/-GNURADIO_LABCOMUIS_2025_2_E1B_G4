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

### Resumen
En esta práctica la misión es crear nuestra propia emisora, esto se logrará mediante la creación de un pequeño bloque de programación para ser transmitido en el campus universitario, que pueda ser sintonizado por cualquier receptor de radio FM estándar. Para esto se utilizó la IA y el software Audacity para crear un archivo de audio el cual haría la interpretación del locutor de la emisora, se combina este audio con una canción llamativa y se mazteriza para asegurar que sea un archivo estéreo. El archivo de audio resultante es el que se transmitirá mediante el USRP para poder ser percibido por dispositivos cuya antena capte señales FM.

**Palabras clave:** Emisora FM, Aucio estéreo, USRP, GNU Radio.

### Introducción
En esta misión el propósito es crear un archivo de audio estéreo el cual deberá ser percibido por dispositivos con antenas capaces de captar señales FM, Esto es lo que llamaremos como "nuestra propia emisora FM". Para la construcción de este archivo de audio y su correcta transmisión se dividió la práctica en las siguientes fases:
  1. Fase inicial.
  2. Fase crítica.
  3. Fase final.

### Fase inicial.
En esta fase se utilizó la IA para para darle cuerpo con una voz llamativa al mensaje que se creó en conjunto con el grupo de trabajo, utilizando una voz llamativa que le diera un tono de locutora de radio. Luego se uso el software de edición de audio Audacity en donde se masterizó y mezcló el audio creado con la IA en conjunto con una canción llamativa para obtener un archivo de audio estéreo resultante muy llamativo y con un estilo a emisora ordinaria, este archivo de audio resultante debía durar de 60 a 90 segundos y será el que se transmitirá para probar la eficiencia de nuestra transmisión


## Fase 2: Construcción
En esta fase, usamos las medidas de la simulación para construir la antena con alambre de cobre y una placa reflectora.

Detalle Importante: La construcción se hizo de forma rústica y no se tuvo cuidado "milimétrico" con las medidas. Esto, como ya se esperaba, significaría que los resultados en el laboratorio no serían totalmente exactos.

<img src="Imagenes/antena.jpg" width="400"> 

## Fase 3: Medición y Validación
Se probó la antena en el laboratorio con dos equipos:

VNA (Vector Network Analyzer): Mide la frecuencia de resonancia.

Analizador de Espectro: Mide la señal recibida y comprueba la directividad.

Resultado 1: Resonancia
Al medir la frecuencia real, se encontró una gran diferencia con respecto a la simulada. La desviación fue de aproximadamente 150 MHz.

<img src="Imagenes/parametro_S11.jpg" width="400"> 

Resultado 2: Frecuencias operacionales encontradas
En la frecuencia de resonancia y asumiendo un ancho de banda de 60 MHz pudimos encontrar dos bandas de frecuencias que se usan para telefonia fija según el Cuadro Nacional de Atribución de Bandas.

<img src="Imagenes/atribucion_espectro.png" width="400"> <img src="Imagenes/espectro_antena_construida.jpg" width="400">

Resultado 3: Funcionalidad (Directividad)
- Para esta prueba, el profesor generó una señal de prueba.
- Conectamos la antena al Analizador de Espectro.
- Al apuntar la antena directamente a la fuente de la señal, la señal en la pantalla aumentó mucho.
- Al moverla, la señal bajaba.

Conclusión Funcional: La antena es totalmente funcional y direccional, tal como se había planeado. Logramos visualizar una banda de frecuencia de televisión en el analizador.

También hicimos una comparación con una antena comercial para determinar la ganancia de la antena construida, la antena comercial tenia una ganancia de 6 dBm, y al comparar con la contruida hayamos una diferencia de 2 dBm al medir con la antena costruida, por lo cual concluimos que esta tiene una ganancia de 4 dBm.

<img src="Imagenes/espectro_señal_ejemplo_antena_construida.jpg" width="400"> <img src="Imagenes/espectro_señal_ejemplo_antena_base.jpg" width="400">

### Análisis y Conclusiones
¿Por qué falló la frecuencia?
- La principal razón de que la frecuencia real no fuera 915 MHz es la construcción imprecisa. En las antenas, la precision es crucial. Al construirla "rústicamente", las dimensiones no fueron exactas.

¿Por qué funcionó la directividad?
- La directividad sí se cumplió porque el concepto de diseño con el reflector es correcto. Aunque la antena no resonó exactamente donde queríamos, la antena es funcional.

Conclusión Final:

El proyecto fue un éxito en su objetivo principal: se demostró que el diseño de la Antena Biquad con reflector crea un patrón direccional. Sin embargo, se confirma que la precisión en la construcción es el factor más crítico para que la antena funcione exactamente en la frecuencia deseada. El ajuste de dimensiones en el programa de simulación (MATLAB) fue vital para encontrar el punto de partida del diseño.

---

Volver al [INICIO](#laboratorio-de-comunicaciones)
