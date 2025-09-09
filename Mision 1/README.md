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
El estudio de señales en el espectro se llevó a cabo utilizando tres instrumentos clave: un SDR, un analizador de espectro y un osciloscopio, cada uno cumpliendo un rol estratégico. La metodología se dividió en tres fases principales.

**Palabras clave:** SDR, Analizador de Espectro, Osciloscopio, Frecuencia, Tiempo. 

### Introducción
Este informe presenta un resumen del trabajo realizado para explorar y analizar las señales de radio que nos rodean. Usamos tres equipos diferentes: un SDR, un analizador de espectro y un osciloscopio. El objetivo era entender cómo se comportan estas señales y qué ventajas tiene cada herramienta para estudiarlas.

El proceso se dividió en tres partes: primero, usamos el SDR para tener una idea general de qué señales hay en el aire. Luego, con el analizador de espectro, hicimos mediciones exactas de la señal que elegimos. Finalmente, intentamos ver la señal con el osciloscopio para entender cómo cambia con el tiempo.

El trabajo nos ayudó a entender que cada equipo es clave en un momento diferente del análisis. Los siguientes puntos detallan lo que encontramos y cómo cada herramienta nos dio una pieza importante del rompecabezas para entender mejor el mundo de las telecomunicaciones.

### Fase 1: Exploración con SDR (Ojo Panorámico)
En esta etapa, se utilizó un SDR para mapear de manera amplia el espectro radioeléctrico. El SDR demostró ser una herramienta eficiente para la exploración, permitiendo la identificación rápida de señales de interés. Durante el barrido, se identificaron múltiples servicios, incluyendo emisoras de radio FM, estaciones AM, y señales no identificadas. Este proceso fue crucial para seleccionar una señal potente y estable para un análisis más detallado.

<img src="imagenes/Captura desde 2025-08-13 17-15-45.png" width="300">  <img src="imagenes/Captura desde 2025-08-13 17-26-22.png" width="300"> <img src="imagenes/Captura desde 2025-08-13 17-27-17.png" width="300">

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
