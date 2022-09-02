# Proyecto T6: Desarrollo de Codificadores de Posición en Transformers

### Profesor: Pablo Estevez V.
### Guía: Bastian Gamboa Labbé

##Descripción:

Los mecanismos de atención son modelos diseñados originalmente para el procesamiento tipo
secuencia-secuencia, los cuales buscan la construcción de vectores de contexto basada en la
estimación de correlaciones lineales entre una colección de vectores “keys” con respecto a
vectores “queries” (dot-attention). Uno de los primeros trabajos en introducir estos mecanismos
fue el realizado por (Bahdanau et al. 2014) [4], quien los utilizó en conjunto con modelos RNN
buscando mejorar el rendimiento de modelos de traducción de lenguaje con secuencias de
texto. Años después, uno de los trabajos más importantes fue presentado por (Vaswani et al.
2017) [2] quien propone el uso de un modelo basado completamente en mecanismos de
atención: el modelo Transformer. Por otro lado, el uso de estos mecanismos, posibilita la
realización de experimentos de interpretabilidad, los cuales resultaron ser muy relevantes para
el área de Natural Language Processing (NLP). Gracias a este trabajo, estos modelos han
ganado una gran popularidad en los últimos años, especialmente en el área de NLP con
modelos como BERT o GTP, pero también ha surgido también el interés por importar estos
modelos para el procesamiento general de series de tiempo.
Sin embargo, estos modelos no presentan un procesamiento secuencial de los datos como las
conocidas redes recurrentes (LSTM o GRU), por lo cual es necesario introducir información
posicional a los datos. En la literatura se han desarrollado diferentes métodos para la
introducción de información posicional, pero no se ha profundizado en detalle cuál de los
algoritmos es mejor acorde la naturaleza del problema. En este trabajo se busca encontrar
alternativas y demostrar mediante pruebas el impacto de la codificación temporal para la
7
clasificación de supernovas. En este trabajo se probarán y-o demostrará la efectividad de cada
uno de los codificadores de posición desarrollados.
El modelo a utilizar corresponde a una arquitectura de AutoEncoder como la presentada en
(Pimentel et al 2022) [1] donde se utilizará como punto de partida la misma codificación
temporal utilizada en este trabajo denominada TimeFiLM, a partir de esta codificación se
deberán de trabajar en al menos cuatro variantes (desarrolladas por el grupo) las cuales deben
de poseer distintas propiedades. Se debe de mostrar cuál es la codificación que se ajusta mejor
al problema. En este proyecto se busca dar respuesta a las siguientes preguntas:
1) ¿Es posible encontrar nuevas formas de entregar información posicional además de
TimeFilm o las que se puede encontrar en la literatura?
2) ¿Se logra apreciar mejoras al realizar diferentes codificaciones (robustez al ruido, mejor
tasa de clasificación)?
3) ¿Es relevante la codificación temporal?
Para comenzar el proyecto, se podrían generar curvas sintéticas basadas en el modelo SPM
que sean fáciles de caracterizar e inspeccionar visualmente, y desarrollar mediante la
clasificación de estas curvas sintéticas diferentes tipos de codificación temporal que den
mejores resultados, tomando como punto de partida la codificación TimeFiLM. Utilizando los
mismos datos sintéticos se validará si los codificadores empleados presentan propiedades
relevantes. ¿Existe una codificación que sea más robusta al ruido ? (Las formas de testear esta
propiedad se pueden realizar en las curvas sintéticas añadiendo ruido en amplitud y tiempo).
Finalmente se deberá emplear dichas modulaciones en la clasificación de Supernovas
provenientes del Zwicky Transient Facilit
