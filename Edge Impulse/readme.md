# Edge-Impulse

Edge-Impulse es una plataforma de desarrollo para *Machine Leraning* en dispositivos edge, gratuita para los desarrolladores y de confianza para las empresas.

![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Edge%20Impulse/thumbnail_edge-impulse_01.png)

## Reconocimiento Comandos de Voz

Se ha utilizado Edge-Impulse para crear la funcionalidad de reconocer comandos de voz introducidos mediante un sensor de audio. 

 ## El [proyecto creado](https://studio.edgeimpulse.com/public/65423/latest) a través de Edge Impulse.
 ### Los pasos seguidos en Edge Impulse son los siguientes

*  Lo primero es conectar un dispositivo a la plataforma para comenzar con la adquisición de datos, en nuestro caso, archivos de audio. En una primera instancia se realizaron grabaciones de 2 segundos para ello. Pero una vez creado el modelo, se comprobó que no era lo suficientemente exacto por la poca cantidad de datos que tenía para el entrenamiento.
*  Para mejorar el modelo, se decidió utilizar *Google Speech Commands Dataset*. Este dataset se utiliza para aplicaciones de deep learning para reconocimiento de voz y de audio, siendo capaz de ayudar a reconocer palabras y comandos. El conjunto de datos cuenta con 65.000 expresiones de un segundo de duración de 30 palabras cortas, realizadas por miles de personas diferentes, aportadas por miembros del público a través del sitio web de AIY. Está publicada bajo una licencia Creative Commons BY 4.0, y seguirá creciendo en futuras versiones a medida que se reciban más contribuciones.

*  Una vez conseguido el dataset, se empieza con el diseño del impulso. Un impulso toma los datos en bruto, utiliza el procesamiento de la señal para extraer características y, a continuación, utiliza un bloque de aprendizaje para clasificar los nuevos datos.
La creación del impulso se puede dividir en tres pasos: primero establecer el tamaño de los datos procesados, en nuestro caso de 1000ms y la frecuencia de muestreo a 16kHz. El segundo paso serían los bloques MFCC de audio que extraen features y aplican parámetros de una señal de audio.

* ##Los features creados son los siguientes:
![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Edge%20Impulse/edge3.png)

* ##Una visualización de los samples es la siguiente:
![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Edge%20Impulse/edge2.png)

* ### Crear la librería en Edge Impulse y migrarla al dispositivo
* ### Mediante PUTTY utilizar el comando: AT+RUNIMPULSE para empezar con la captación de datos 

* ### El [Excel](https://docs.google.com/spreadsheets/d/1DuhQhVBs4jBqO62ucJH18hLz-siLDMmFLaAkOy_AL4A/edit#gid=956814287) con los comandos de voz en Drive.

![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Edge%20Impulse/edge.JPG)
