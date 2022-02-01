# Edge-Impulse

Edge-Impulse es una plataforma de desarrollo para *Machine Leraning* en dispositivos edge, gratuita para los desarrolladores y de confianza para las empresas.

![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Edge%20Impulse/thumbnail_edge-impulse_01.png)

## Reconocimiento Comandos de Voz

Se ha utilizado Edge-Impulse para crear la funcionalidad de reconocer comandos de voz introducidos mediante un sensor de audio. Existe un [tutorial](https://docs.edgeimpulse.com/docs/responding-to-your-voice) disponible para esta aplicación. 

 ## El [proyecto creado](https://studio.edgeimpulse.com/public/65423/latest) a través de Edge Impulse.
 ### Los pasos seguidos en Edge Impulse son los siguientes

*  Lo primero es conectar un dispositivo a la plataforma para comenzar con la adquisición de datos, en nuestro caso, archivos de audio. En una primera instancia se realizaron grabaciones de 2 segundos para ello. Pero una vez creado el modelo, se comprobó que no era lo suficientemente exacto por la poca cantidad de datos que tenía para el entrenamiento.
*  Para mejorar el modelo, se decidió utilizar [*Google Speech Commands Dataset*](https://dax-cdn.cdn.appdomain.cloud/dax-tensorflow-speech-commands/1.0.1/data_preview/notebooks.html). Este dataset se utiliza para aplicaciones de deep learning para reconocimiento de voz y de audio, siendo capaz de ayudar a reconocer palabras y comandos. El conjunto de datos cuenta con 65.000 expresiones de un segundo de duración de 30 palabras cortas, realizadas por miles de personas diferentes, aportadas por miembros del público a través del sitio web de AIY. Está publicada bajo una licencia Creative Commons BY 4.0, y seguirá creciendo en futuras versiones a medida que se reciban más contribuciones. Disponible para su [descarga](https://dax-cdn.cdn.appdomain.cloud/dax-tensorflow-speech-commands/1.0.1/tensorflow-speech-commands.tar.gz).

*  Una vez conseguido el dataset, se empieza con el diseño del impulso. Un impulso toma los datos en bruto, utiliza el procesamiento de la señal para extraer características y, a continuación, utiliza un bloque de aprendizaje para clasificar los nuevos datos.
La creación del impulso se puede dividir en tres pasos: primero establecer el tamaño de los datos procesados, en nuestro caso de 1000ms y la frecuencia de muestreo a 16kHz. El segundo paso serían los bloques MFCC de audio que extraen features y aplican parámetros de una señal de audio.

* #### Los features creados son los siguientes:
![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Edge%20Impulse/edge3.png)

* #### En la siguiente imagen se muestra una visualización de los samples:
![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Edge%20Impulse/edge2.png)

*  Como tercer paso, Con todos los datos procesados es hora de empezar a entrenar una red neuronal, *NN Classifier*. La red que estamos entrenando tomará el MFCC como entrada y tratará de asignarlo a una de las tres clases: la palabra clave, el ruido o lo desconocido. 

* #### Como resultado de modelo se consigue el siguiente rendimiento:
![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Edge%20Impulse/train.png)

*  Una vez creado y analizado todo, es hora de probar la funcionalidad mediante un dispositivo externo. En nuestro caso, utilizamos la SiLabs Thunderboard Sense 2 y su sensor de audio para captar nuestros comandos de voz en tiempo real. Edge Impulse empaqueta el impulso completo, desde el código de procesamiento de la señal hasta el modelo entrenado, y lo desplegamos en nuestro dispositivo. Esto garantiza que el impulso se ejecute con baja latencia y sin requerir una conexión de red.

*  Se crea la librería en Edge Impulse la cual se migra al dispositivo y mediante PUTTY utilizamos el comando AT+RUNIMPULSE para empezar con la captación de datos. Finalmente se comprobó que la aplicación funciona correctamente para los comandos con más samples, ya que para otros se confundía y no distingue con mucha exactitud entre unos y otros.

* #### El [Excel](https://docs.google.com/spreadsheets/d/1DuhQhVBs4jBqO62ucJH18hLz-siLDMmFLaAkOy_AL4A/edit#gid=956814287) generado con los comandos de voz en Drive.

*  En la siguiente imaagen se muestra el rendimiento del modelo de manera visual con todos los tipos de samples.
![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Edge%20Impulse/edge.JPG)
