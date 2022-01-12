## Arquitectura flujo Tableau

Los comandos de voz se simulan con un periodo de 15 minutos a través de node-red ya que no se tienen datos en tiempo real desde los ascensores, entonces la subida de datos de los comandos de voz está automatizada a un excel en drive a través de node-red y desde ese excel se leen y analizan para luego analizar kpis en Tableau.

* ### El [Excel](https://docs.google.com/spreadsheets/d/1DuhQhVBs4jBqO62ucJH18hLz-siLDMmFLaAkOy_AL4A/edit#gid=956814287) con los comandos de voz en Drive.

* ### El diseño del flujo [Node red](https://8tomf0.stackhero-network.com/admin/#flow/e5135e566cac99ad) creado desde el link de Moodle.

El documento Ascensore Ermua.twb es el programa creado en Tableau que utiliza tanto los datos extraidos del excel de los comandos de voz como los del excel "Datos_ascensores_dic_2021" proporcionado por Iván Arakistain en clase. 
Utilizando estos datos se ha creado un Dashboard que se ha compartido en [Tableau Public](https://public.tableau.com/views/AscensoresErmua/DIGITALTWINDELOSASCENSORESPUBLICOSDEERMUA?:language=es-ES&publish=yes&:display_count=n&:origin=viz_share_link:showVizHome=no#1)

También se han incluido las imagenes utilizadas en el Dashboard
