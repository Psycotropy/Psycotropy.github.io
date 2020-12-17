---
layout: post
title:  "Crear texturas para fs2004"
date:   2020-12-13 19:48:56 -0300
categories: texturas aviones fs2004 repaints
permalink: /post/crear-texturas-fs2004/
---
Como hacer un repaint es una tarea que va desde lo mas facil en temas de programas y manejo de los archivos 
a pesar de algunos trucos para realizar la tarea. A continuacion mostrare los pasos a seguir con un repaint
de project airbus para sky airlines. Una de las cosas principales a la hora de pintar es tener clara la 
diferencia entre un paint kit un archivo bmp y la compresion DXT para texturas y capas de pintado. 
estas son algunas de las mas importantes las otras las iremos viendo mas abajo.
- **PaintKit**: son archivos que para el caso del Fs2004 estan exportados generalmente en bmp, estos se caracterizan
por ser un repintado blanco para el avion, la mayoria de las veces se encuentran hechos por los fabricantes de los modelos
de aviones para simuladores como ocurre con [Project airbus](https://www.pafs.wf/downloads).
![a320 project airbus](\img\posts\crear-texturas-fs2004\a320blankModelConverter.JPG) ***A320 de Project airbus pintado con el paintkit que ofrece la
pagina oficial desplegado en el programa de visualizacion de modelos [Model Converter X](https://www.scenerydesign.org/modelconverterx/)***.

![a320 blanco aterrizando](\img\posts\crear-texturas-fs2004\a320blank.JPG) ***Se puede inferir que los paintkit generalmente imitan a una "livery" que 
debe ser pintada, como se muestra en la imagen del a320 aterrizando el cual es un avion que debe ser pintado, esa es la idea con la que se crea un kit de pintado***.

- **Archivo .bmp**: en wikipedia [hay un articulo que los enseña correctamente](https://es.wikipedia.org/wiki/Windows_bitmap), pero que para efectos practicos
del repintado en fs2004 este es el formato estandar con el que se exporta una pintura para ser usada en el juego, cabe señalar que en el Fsx exite otro formato 
llamado dds que es incompatible si se usa en su homologo antesesor del cual trata el articulo.

- **Compresion DXT**: Aunque esta en ingles [esta wiki](https://www.fsdeveloper.com/wiki/index.php?title=Texture_formats_overview) sirve para hacerse una idea
de lo que trata, en el articulo lo usaremos en la parte final cuando debamos traspasar nuestras texturas recien creadas al juego.

# Montando el entorno de creacion 

Luego de que hayamos descargado el modelo a trabajar junto con nuestro paint kit o bien usemos texturas ya descargadas para editarlas y hacer la nuestra, lo cual es una via alternativa
mas facil y rapida en caso de no encontrar un paintkit de calidad. En segundo lugar tambien necesitaremos tener instalado en su ultima version [GIMP](https://www.gimp.org/downloads/) 
que es una alternativa antigua, robusta y facil de usar al ya conocido adobe Photoshop. Tambien finalmente deberemos tener [Paint .NET](https://www.getpaint.net/download.html) (el paint de toda la vida) o un equivalente que permita comprimir y manejar archivos en formato DXT. 
Una vez con el cuadrangular instalado correctamete en nuestra computadora procederemos con manos a la obra. 

# Empezando a crear nuestra textura
Primero seleccionaremos y recluiremos a un directorio aparte solo los elementos necesarios para llegar a nuestro objetivo que es un airbus A320 con motores CFM de la compañia
Sky airlines. Copiaremos a un directorio de trabajo los siguientes archivos:

![directorio paintkit](\img\posts\crear-texturas-fs2004\paintkitSinFiltrar.JPG)***Vista del directorio inmediatamente despues de haber extraido el paintkit del RAR***.

![directorio paintkit](\img\posts\crear-texturas-fs2004\abrirPSDGimp.JPG)***Abrimos la textura que vayamos a trabajar en este caso la de los motores cfm que se conoce como A320_2_t.psd***.

![directorio paintkit](\img\posts\crear-texturas-fs2004\ExportarAPSDaBMP.JPG)***Una vez abierto el gimp (en este caso en su version 2.10.12), le damos en el menu superior a lo siguiente Archivo 
 | Exportar como; y una vez alli solamente basta con seleccionar el directorio donde estamos dejando nuestras texturas y posteriormente cambiar la extension .psd por .bmp y finalemente click izquerdo en exportar. Repetimos el proceso con todas las imagenes que necesitemos, que en el caso de nuestro a320 necesitaremos todas las que aparecen en la foto de abajo ¡IMPORTANTE! 
 no cambiar los nombres originales solamente la extension.***

![directorio de repaint despues de la seleccion](\img\posts\crear-texturas-fs2004\paintkitFiltrado.JPG)***Directorio sobre el cual he generado una textura trabajable que corresponde 
al a320 cfm de la primera imagen del articulo, debo mencionar que las texturas de las alas se pueden copia y pegar de un freeware para ahorrar tiempo ya que todas se parecen y si se quieren editar se pueden hacer perfectameten con solo algunos cambios en el GIMP.***

# Soltando la brocha
En esta parte no puedo explicar un procedimiento paso por paso por temas de extension del articulo, ademas que es una trabajo que requiere creatividad, por no mencionar que es una habilidad que se adquiere en el tiempo. Pero eso no impide que explique algunas de las cosas mas importantes que nos permitiran hacer nuestra textura de la mejor manera.

- **Como pintar**: Hay herramientas en el GIMP con las cuales nos aliaremos para poder hacer nuetro repaint se mencionan a continuacion: La herrmienta pincel que nos servira para hacer los acabados grandes y detallados, algo interesante de esta herramienta es la manera en la que se pueden hacer las lineas rectas haciendo click sobre el punto donde inicia, luego apretando SHIFT y finalemente haciendo click donde queremos terminar nuestra linea recta; La herramienta de texto, muy buena para hacer las tipografias del avion.

![exhibicion de herramientas de pintado](\img\posts\crear-texturas-fs2004\gimpExplicacionPincel.JPG) ***Se muestran las heramientas se puede acceder a ellas haciendo doble click en la deseada***.

- **Herramientas de transformacion**: Estas a diferencia de otros programas no estan integradas en el cuadro de texto por ejemplo, pero se pueden seleccionar en el menu superior en Herramientas herramientas de seleccion y herramientas de transformacion son las que mas se utilizan para este punto.

# Ejemplo 

Ahora veremos todo lo que habria que hacer para pintar nuestra turbina con los colores de Skyairline como se ve en la imagen:![motor sky](\img\posts\crear-texturas-fs2004\letrasSky.jpg) 

Lo primero es en abrir el bmp que anteriormente ya creamos y con la herramienta de texto hacemos un cuadro sobre la turbina como se muestra en la foto:![pintado](\img\posts\crear-texturas-fs2004\muestraDepintado.jpg)

Es importante que rotemos la imagen como se aprecia en la imagen de abajo para que luzca como arriba si no se hace al momento de desplegarla se vera al reves cosa que no queremos 
![rotacion](\img\posts\crear-texturas-fs2004\rotacionPintado.jpg)

Ahora antes de pasarla al flight simulator debemos ver como luce en model converter para esto yo tengo un directorio aparte justo donde descargue el modelo 3d de Project airbus a320-214 ahi tengo una Textura de Lan chile, Sky airline y ahora la blank el directorio ubicado en E:\Microsoft Games\Flight Simulator 9\Aircraft\Project Airbus A320-214 es obligacion que la carperta donde pongamos las texturas este en el fomato texture.nombre como se ve a continuacion:
![ubicaciona320-214](\img\posts\crear-texturas-fs2004\directorioModelo.JPG) 

Para que la textura sea detectada por el model converter y luego por el FS2004 debemos agregar el siguiente texto al aircraft.cfg que es solamente un archivo que los programas encargados de generar la textura leen y segun eso funcionan todas las lineas son totalmente editables, lo mas importante es la parte que dice texture que debe ser el mismo nombre despues del . de la carpeta texture en el directorio de nuestro avion de lo contrario no funcionara

[fltsim.2]

title=Project Airbus A320-214 BLANK CFM

ui_variation=BLANK VERSION

sim=pa320-cfm56

model=

panel=

sound=

texture=Blank

checklists=

description=Project Airbus A320\n\n\n\n\n\n Livery blank

atc_id=9H-AEI

atc_airline=airbus

atc_flight_number=451

ui_manufacturer=Project Airbus A320 CFM

ui_type=A320-214

visual_damage=1

atc_heavy=0

Ahora en el model converter abrimos el archivo .model ubicado en la carpeta model y seleccionamos la textura que el programa nos ofrece, mas detalles en la imagen:
![a320enmodelconverter](\img\posts\crear-texturas-fs2004\a320pintado.JPG)

Bien ahora que ya que tenemos una textura visualizable que nos gusta nos acercamos a la recta final de este manual, si ahora se nos ocurre ir a jugar con nuestra nueva textura nos dariamos cuenta de un gran problema porque nos encontrariamos con esto
![a320comprimidoendds](\img\posts\crear-texturas-fs2004\a320malo.png) 

Queee!!! pero que significa eso, entonces perdi todo el tiempo gracias por el buen manual te lo lanzare por la cabeza. Momento a calmarse porque ahora es cuando entran en accion los chicos malos del PAINT, y de la compresion DXT mas especificamente la DXT3. Procederemos de la siguiente forma con PAINT abriremos uno por uno los archivos en la carpeta texture.BLANK y los guardaremos en la misma carperta con el mismo nombre para reemplazar a los que teniamos, pero atentos porque haremos esto que causara la diferencia en la parte de Tipo eligiremos la opcion Mapa de bits de 24 bits (*.bmp;.dib) como hago aqui:
![texturaCompresion](\img\posts\crear-texturas-fs2004\correccionDXT.JPG)
Una vez terminemos el proceso se deberia poder visualizar correctamente. Si el paint muestra un cartel de que la imagen perdera transparencia al guardar le damos a aceptar. Ahora en la imagen el avion se puede visualizar correctamente pudiendose incluso visualizar el texto que pusimos en las turbinas.
![avion corrceto](\img\posts\crear-texturas-fs2004\avioncorrecto.png)
Ahora lo volaremos, como project airbus no trae cabina incluida le agregare una que tengo de otro avion, lo mismo con los sonidos. Para lo anterior en las carpetas panel y sound hare lo siguiente modificare en las lineas de los archivos que las preceden dejando los archivos asi:

- archivo panel.cfg: alias=LATAM-A320-214-sharklet-CC-BAT/panel o bien si no tienes un avion con panel instalado puedes usar el de el 737 default asi alias=b737_400/panel

- archivo sound.cfg: alias=LATAM-A320-214-sharklet-CC-BAT/sound o el sonido del 737 default asi alias=b737_400/sound

Volarlo se ve así con algunas capturas en el aeropuerto Arturo Merino Benitez de Santiago.



