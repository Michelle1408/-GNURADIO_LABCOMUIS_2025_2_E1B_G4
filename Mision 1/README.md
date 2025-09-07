# Laboratorio de Comunicaciones
## Universidad Industrial de Santander

---
# Misión 1: Reconocimiento de Equipos y Espectro

### Integrantes
- **MICHELLE GARZÓN CAMPOS** - 2202785
- **SEGUNDO INTEGRANTE** - Código

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
Descripción en no más de 150 palabras del contenido de la práctica. Debe ser conciso y brindar una idea clara sobre el trabajo realizado y sus conclusiones.

**Palabras clave:** de 2 a 5 palabras clave. 

### Introducción
Este informe presenta un resumen del trabajo realizado para explorar y analizar las señales de radio que nos rodean. Usamos tres equipos diferentes: un SDR, un analizador de espectro y un osciloscopio. El objetivo era entender cómo se comportan estas señales y qué ventajas tiene cada herramienta para estudiarlas.

El proceso se dividió en tres partes: primero, usamos el SDR para tener una idea general de qué señales hay en el aire. Luego, con el analizador de espectro, hicimos mediciones exactas de la señal que elegimos. Finalmente, intentamos ver la señal con el osciloscopio para entender cómo cambia con el tiempo.

El trabajo nos ayudó a entender que cada equipo es clave en un momento diferente del análisis. Los siguientes puntos detallan lo que encontramos y cómo cada herramienta nos dio una pieza importante del rompecabezas para entender mejor el mundo de las telecomunicaciones.

### Fase 1: Exploración con SDR (Ojo Panorámico)
En esta etapa, se utilizó un SDR para mapear de manera amplia el espectro radioeléctrico. El SDR demostró ser una herramienta eficiente para la exploración, permitiendo la identificación rápida de señales de interés. Durante el barrido, se identificaron múltiples servicios, incluyendo emisoras de radio FM (como Radio Policía Nacional en 91.7 MHz), estaciones AM, telefonía móvil (800 MHz), flotas de taxis (780 MHz), televisión digital terrestre (490 MHz) y sistemas de radio troncalizados (858 MHz). Este proceso fue crucial para seleccionar una señal potente y estable para un análisis más detallado.

## Fase 2: Análisis de Precisión con Analizador de Espectro
Una vez seleccionada la señal, el analizador de espectro se utilizó para mediciones precisas en el dominio de la frecuencia. Se configuraron parámetros como el SPAN y el RBW para obtener una visión detallada de la señal. Se registró una frecuencia central exacta de 91.7 MHz, una potencia de 48.84 dBm y un ancho de banda de 3.384 kHz. El analizador de espectro se confirmó como el instrumento más adecuado para obtener datos de potencia y ancho de banda confiables, superando al SDR en precisión y al osciloscopio en la visualización del espectro de frecuencia.

## Fase 3: Visualización en el Dominio del Tiempo con Osciloscopio
Esta fase fue la más desafiante. La señal de RF, al contener múltiples frecuencias y ruido, resultó en una forma de onda "aleatoria" en la pantalla del osciloscopio. Se midió un voltaje pico a pico de 15.5 mV, pero la frecuencia no pudo ser determinada con exactitud debido a las fluctuaciones. La principal dificultad fue la ausencia de un filtro previo, lo que impedía aislar la señal de interés de otras perturbaciones. Se concluyó que el osciloscopio, por sí solo, no es la herramienta ideal para el análisis de una señal de RF del aire sin un filtrado o un circuito de down-conversion que la baje a una frecuencia manejable.

### Conclusiones
La combinación de los tres equipos es esencial para un análisis completo de las señales de RF. El SDR es inigualable para la exploración y el descubrimiento inicial. El analizador de espectro es la herramienta de elección para mediciones precisas en el dominio de la frecuencia. Finalmente, el osciloscopio es fundamental para el análisis en el dominio del tiempo, siempre y cuando la señal de entrada esté adecuadamente preparada. El "pico" en el analizador de espectro representa la concentración de potencia de la señal en una frecuencia específica, lo cual se correlaciona con la forma de onda sinusoidal que se observa en el osciloscopio, representando su comportamiento a lo largo del tiempo. 

### Referencias
Ejemplo de referencia:

- [Proakis, 2014] J. Proakis, M. Salehi. Fundamentals of communication systems. 2 ed. England: Pearson Education Limited, 2014. p. 164-165, 346. Chapter 5 In: [Biblioteca UIS](https://uis.primo.exlibrisgroup.com/permalink/57UIDS_INST/63p0of/cdi_askewsholts_vlebooks_9781292015699)

---
# Ejemplos usando Markdown

Volver al [INICIO](#laboratorio-de-comunicaciones)

## Inclusión de Imágenes
### Imagen de referencia dentro del repositorio:
![Networking](my%20file/test.png)

### Imagen de fuente externa
![GNU Radio logo](https://kb.ettus.com/images/thumb/5/50/gnuradio.png/600px-gnuradio.png)

### Uso de html para cambiar escala de la imagen
<img src="https://kb.ettus.com/images/thumb/5/50/gnuradio.png/600px-gnuradio.png" alt="GNU Radio Logo" width="300">

## Creación de hipevínculos 
- [Aprende Markdown](https://markdown.es/)
- [Más acerca de Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
- [Abrir documento en el repositorio](my%20file/test_file.txt). Si hay espacios en la ruta de su archivo, reemplácelos por `%20`.
- Ir a una sección de este documento. Por ejemplo: [Ir a Contenido](#contenido) Tenga en cuenta escribir el título de la sección en minúsculas y los espacios reemplazarlos por guiones.
## Uso de Expresiones Matemáticas
Se pueden incluir ecuaciones en el archivo `README.md` utilizando sintaxis similar a [LaTeX](https://manualdelatex.com/tutoriales/ecuaciones):

### Ecuaciones en Línea
```
La energía de una señal exponencial es $E = \int_0^\infty A^2 e^{-2t/\tau} dt$.
```
**Salida renderizada:**
La energía de una señal exponencial es $E = \int_0^\infty A^2 e^{-2t/\tau} dt$.

### Ecuaciones en Bloque
```
$$E = \int_0^\infty A^2 e^{-2t/\tau} dt = \frac{A^2 \tau}{2}$$
```
**Salida renderizada**
$$E = \int_0^\infty A^2 e^{-2t/\tau} dt = \frac{A^2 \tau}{2}$$

## Creación de Tablas

**Tabla 1.** Ejemplo de tabla en Markdown.

| Parámetro | Valor |
|-----------|-------|
| Frecuencia (Hz) | 1000 |
| Amplitud (V) | 5 |
| Ciclo útil (%) | 50 |

## Inclusión de código

```python
def hello_world():
    print("Hello, World!")
```

También es posible resaltar texto tipo código como `print("Hello, World!")`.

---

Volver al [INICIO](#laboratorio-de-comunicaciones)
