# Laboratorio de Comunicaciones
## Universidad Industrial de Santander

---
# Misión 1: Reconocimiento de Equipos y Espectro

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
En esta ocasión tratamos de diseñar, construir y probar una antena llamada Biquad con reflector. El objetivo era que funcionara a una frecuencia de 915 MHz y que fuera direccional para captar mejor las señales. Usamos MATLAB para simular las dimensiones ideales, y luego se sontruyó con alabre de cobre y un reflector. Debido a la falta de precisión, la frecuencia de resonancia no fue la misma a la simulada, sin embargo, se demostró que la antena es totalmente funcional.

**Palabras clave:** SDR, Analizador de Espectro, Osciloscopio, Frecuencia, Tiempo. 

### Introducción
Este informe explica cómo se creó una Antena Biquad con un reflector. El diseño se basa en la idea de que dos cuadrados de alambre (los "quads") captan la señal, y una placa metálica detrás (el reflector) empuja toda esa energía hacia adelante. Esto hace que la antena tenga más potencia en una dirección.
El proceso se dividió en tres partes:
1) Diseño: Calcular y simular las medidas perfectas en la computadora.
2) Construcción: Fabricar la antena con las medidas obtenidas.
3) Medición: Probar la antena con equipos de laboratorio para ver si funcionaba.

### Fase 1: Diseño y Simulación (La Receta)
Para que la antena funcionara a 915 MHz, utilizamos MATLAB para estiamr el tamaño de los cuadrados de alambre y la distancia del reflector.

Ajuste Fino: Usamos el programa MATLAB (Antenna Designer) para simular la antena. Fue como un "prueba y error" digital: primero dejamos que el programa estimara las medidas y luego fuimos modificando el tamaño de los lados y la distancia al reflector hasta que el programa nos dijo que la antena resonaría justo en 915 MHz.

Medidas Ideales (Simuladas):
Lado del cuadrado de alambre: 8.55 cm
Distancia al reflector: 4 cm
Frecuencia esperada: 915 MHz

<img src="imagenes/antena_matlab" width="300"> 

El patrón de radiación simulado confirmó que la antena debería ser direccional (tendría un lóbulo grande hacia adelante).


## Fase 2: Análisis de Precisión con Analizador de Espectro
Una vez seleccionada la señal, el analizador de espectro se utilizó para mediciones precisas en el dominio de la frecuencia. Se configuraron parámetros como el SPAN y el RBW para obtener una visión detallada de la señal. Se registró una frecuencia central exacta de 91.7 MHz, una potencia de 48.84 dBm y un ancho de banda de 3.384 kHz. El analizador de espectro se confirmó como el instrumento más adecuado para obtener datos de potencia y ancho de banda confiables, superando al SDR en precisión y al osciloscopio en la visualización del espectro de frecuencia.

<img src="imagenes/Captura de pantalla 2025-09-07 150124.png" width="400"> 

## Fase 3: Visualización en el Dominio del Tiempo con Osciloscopio
Esta fase fue la más desafiante.La frecuencia no es posible de calcular con exactitud con solo el osciloscopio, ya que la señal "senoidal" acumula todas las frecuencias del espectro, lo que la hace fluctuar demasiado. Entre las características de la señal que se ve en el osciloscopio, vemos una señal bastante aleatoria, con mucha distorsión y que no se le pude hacer ningún estudio con solo la ayuda visual, para poder hacer las respectivas medidas se necesita hacer de filtrado para poder elegir frecuencias especificas y poder hacer su respectivo análisis. Se concluyó que el osciloscopio, por sí solo, no es la herramienta ideal para el análisis de una señal sin un filtrado.

<img src="imagenes/Captura de pantalla 2025-09-07 150136.png" width="400"> 

### Conclusiones
La combinación de los tres equipos es esencial para un análisis completo de las señales del espectro. El SDR es inigualable para la exploración y el descubrimiento inicial. El analizador de espectro es la herramienta de elección para mediciones precisas en el dominio de la frecuencia. Finalmente, el osciloscopio es fundamental para el análisis en el dominio del tiempo, siempre y cuando la señal de entrada esté adecuadamente preparada. El "pico" en el analizador de espectro representa la concentración de potencia de la señal en una frecuencia específica, lo cual se correlaciona con la forma de onda sinusoidal que se observa en el osciloscopio, representando su comportamiento a lo largo del tiempo. 

---

Volver al [INICIO](#laboratorio-de-comunicaciones)
