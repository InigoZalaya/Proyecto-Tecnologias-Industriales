# Node-Red

Node-Red es una herramienta de desarrollo basada en flujo para programación visual, para conectar dispositivos de hardware, API y servicios en línea como parte de Internet of Things.

![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Node-Red/Node-red-icon.png)

## Diseño

Se ha utilizado Node-Red para dos crear dos funcionalidades: primero para la adquisición, procesamiento y envío de comandos de vox

 ### El diseño del flujo [Node red](https://8tomf0.stackhero-network.com/admin/#flow/e5135e566cac99ad) creado desde el link de Moodle.
 
 *  Primero se crea un flujo sencillo para empezar a simular valores de probabilidad para los comandos de voz. El primer nodo genera la estructura en formato *.json* con todos los datos de los comandos de voz, para luego ser procesados
![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Tableau/Captura.JPG)

 #### Se incluye la imagen del diseño del flujo y nodos.

![alt text](https://github.com/InigoZalaya/Proyecto-Tecnologias-Industriales/blob/main/Node-Red/nodered.png)

*   Donde se simula que los comandos de voz entran por los distintos ascensores, mediante el nodo *function* se generan aleaotiamente dichos comandos de voz, asignando un valor entre 70-90% de probabilidad de acierto del reconocimiento de voz.
*   Dichos valores se envían a través de la http request y mediante un formulario y una hoja excel se guardan automáticamente en Drive.
 #### El [Excel](https://docs.google.com/spreadsheets/d/1DuhQhVBs4jBqO62ucJH18hLz-siLDMmFLaAkOy_AL4A/edit#gid=956814287) creado a partir de los comandos de voz aleatorios de Node-Red.
