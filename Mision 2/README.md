# Práctica 2: EL ENLACE CRÍTICO

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
En la práctica 2 se busca comparar la potencia de una señal configurada previamente al analisis, dependiendo de la longitud del cable usado para transmitir la señal desde el generador de señales hacia el analizador de espectro, este analisis de dividió en tres fases las cuales seran descritas en este informe.

**Palabras clave:** Potencia, Longitud, Atenuación, Espectro. 

### Introducción
En esta misión el objetivo es hacer una comparación y observar el comportamiento de una señal elegida cuando esta se transmite por cables de diferentes longitudes aunque la misma referencia (RG-58AU), además de otros aspectos lo que principalmente se buscaba era la comparación y el análisis de la potencia registrada por la señal en el analizador de espectro cuando esta se transmitia por dos cables de longitudes diferentes.
para poder cumplir con los objetivos, la misión se dividió en 3 fases en las que a grandes rasgos primero se generó una señal que luego seria transmitida al analizador de espectro para hacer una comparación del espectro debido a cada cable.
En la misión se encotraron resultados intersantes y que denotan una diferencia en las características de la señal cuando esta se transmite por cables de diferentes longitudes

### Fase 1: Establecimiento de la Línea Base (Calibración)
Para esta fase se utilizó el generador de señales junto con el software "GNU radio", con estos instrumentos se estableció una señal que luego fue emitida a una frecuencia de 200 [MHZ] al analizador es espectros para medir su potencia, para esta transmisión se utilizó un cable corto y de buena calidad. la potencia encontrada sera el valor de la potencia de entreda y sera el punto de comparación para todas las demás mediciones con otros cables. (Potencia de entrada: -30.23 [dBm])
<img src="imagenes/Captura de pantalla 2025-09-04 203649.png" width="400"> 

### Fase 2: Pruebas de Campo (Medición de Componentes)
Luego tener el registro de la señal de referencia y su potencia, es decir la que será la potencia de entrada, se desconecto el cable corto y se transmitio la señal por el primer cable (RG-58AU de 80[ft]) para esta vez registar nuevamente la señal en el analizador de espectros, con este primer cable la señal entrego una potencia de -36.64[dBm]. Teniendo este registro se desconecto ahora el primer cable para transmitir la señal por el segundo cable (RG-58AU de 136[ft]) Y realizar el mismo procedimiento, la potencia que entrego la señal transmitida por este segundo cable fue de -42.01 [dBm].
<img src="imagenes/Captura de pantalla 2025-09-04 203855.png" width="400">  <img src="imagenes/Captura de pantalla 2025-09-04 203926.png" width="400"> 

### Fase 3: Diagnóstico y Análisis
Para la fase 3 se busca hacer una comparación de los resultados obtenidos con cada cable utilizado en la fase 2, para esto se realizó los mismos estudios mencionados anteriormente en la fase anterior, con los cables RG-58AU de 80[ft] y RG-58AU de 136[ft] añadiendo nuevos registros usando otras frecuencias. En este punto tambien se busca calcular y comparar el valor de la atenuación para cada cable en cada frecuencia estidiada. los resultaros estan registrados en la siguiente tabla:
| Cable | Frecuencia (MHz) | P_in (dBm) | P_out (dBm) | Atenuación (dB) | 
| :------ | :--------------------| :------------ | :-------------- | :------------------| 
| cable 1|          100              |    -30.23      |      -33.89      |           3.66          | 
| cable 1|          200              |    -30.23      |      -36.64      |          6.41           | 
| cable 1|          500              |    -30.23      |      -41.28      |          11.05         | 
| cable 2|          100              |    -30.23      |      -37.57      |           7.34          | 
| cable 2|          200              |    -30.23      |      -42.01      |          11.78         | 
| cable 2|          500              |    -30.23      |      -50.17      |          19.94         |

### Conclusiones
Se sintetizan los principales aportes y puntos relevantes de la práctica, evitando repetir lo ya consignado en las otras secciones del informe. 

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
