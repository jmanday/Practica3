Practica3
=========

<pre>
Autor: Manuel Jesús García Manday
</pre>

En este documento expondré los pasos realizados y herramientas utilizadas para la realización de la tercera práctica de la asignatura.


<br>
<h3>En que consiste</h3>
En la presenta práctica he creado dos máquinas virtuales básicas (debian7 y ubuntu1310) a partir de las cuales he ido modificando sus propiedades (ram y cpu) para ver como varía su comportamiento frente a las distintas peticiones desde la máquina anfitriona a la aplicación que servirán dichas máquinas.

<br>
<h3>La aplicación</h3>
Para complementar la práctica he realizado una aplicación web en python donde se pueden realizar una serie de acciones tales como inicio de sesión, registros de nuevos usuarios, búsqueda de usuarios, etc. La aplicación trabaja sobre una base de datos no relacional como es **mongodb** donde se almacena los datos de los nuevos usuarios. Toda la implementación de la aplicación esta basada sobre el marco **webpy** que no es mas que un framework para Python de uso sencillo pero lo suficientemente potente para permitir desarrollar una aplicación web en poco tiempo.

<br>
<h3>Máquinas Virtuales</h3>
Como he indicado anteriormente, me he creado dos máquinas virtuales, a las que les he ido modificando propiedades tanto de cpu como de memoria. Para la creación de ambas he usado **vmware** ya que **virtualbox**  no me terminaba de arrancar en mi máquina, y con **windows azure** he tenido problemas para acceder a la máquina virtual creada alli debido a la verificación de claves ssh.

<br>
<h4>Ubuntu13.10</h4>

He realizado una instalación de Ubuntu13.10 básica siguiendo los siguiente pasos:

![imagen134](https://github.com/jmanday/Imagenes/blob/master/imagen134.png?raw=true)

![imagen135](https://github.com/jmanday/Imagenes/blob/master/imagen135.png?raw=true)

![imagen136](https://github.com/jmanday/Imagenes/blob/master/imagen136.png?raw=true)

![imagen137](https://github.com/jmanday/Imagenes/blob/master/imagen137.png?raw=true)

![imagen138](https://github.com/jmanday/Imagenes/blob/master/imagen138.png?raw=true)

![imagen139](https://github.com/jmanday/Imagenes/blob/master/imagen139.png?raw=true)

Dicha máquina posee las características de:

* 512MB de RAM
* 1 procesador
* 1 núcleo

![imagen140](https://github.com/jmanday/Imagenes/blob/master/imagen140.png?raw=true)

 Las tres modificaciones que he realizado a dicha máquina han sido las siguientes:

![imagen141](https://github.com/jmanday/Imagenes/blob/master/imagen141.png?raw=true)

![imagen142](https://github.com/jmanday/Imagenes/blob/master/imagen142.png?raw=true)

![imagen143](https://github.com/jmanday/Imagenes/blob/master/imagen143.png?raw=true)


<br>
<h4>Debian7</h4>

Para la creación de esta otra máquina virtual he realizado los mismo pasos que con la anterior, por lo que no es necesario mostrar imagen al respecto. Las características son las báscicas:

* 512MB de RAM
* 1 procesador
* 1 núcleo

![imagen144](https://github.com/jmanday/Imagenes/blob/master/imagen144.png?raw=true)


No obstante, a esta máquina virtual también le he realizado las mismas modificaciones que hice anteriormente a la máquina de ubuntu.

![imagen145](https://github.com/jmanday/Imagenes/blob/master/imagen145.png?raw=true)

![imagen146](https://github.com/jmanday/Imagenes/blob/master/imagen146.png?raw=true)

![imagen147](https://github.com/jmanday/Imagenes/blob/master/imagen147.png?raw=true)


<h3>Servicios utilizados</h3>
Para echar a andar la aplicación en cualquiera de las máquinas virtuales creadas, hay que instalar una serie de servicios que son de vital importancia para que el programa funcione correctamente. En este caso para cada máquina virtual he instalado las siguiente aplicaciones:

* **git:** mediante la cual me descargo de los repositorios correspondiente a otras aplicaciones como son **webpy** y **pymongo.**

![imagen148](https://github.com/jmanday/Imagenes/blob/master/imagen148.png?raw=true)

	
* **webpy:** framework para Python el cual me lo descargo de su repositorio y la instalo:

![imagen149](https://github.com/jmanday/Imagenes/blob/master/imagen149.png?raw=true)

![imagen150](https://github.com/jmanday/Imagenes/blob/master/imagen150.png?raw=true)


* **mongodb:** sistema de base de datos basado en documentos.

![imagen151](https://github.com/jmanday/Imagenes/blob/master/imagen151.png?raw=true)


* **pymongo:** biblioteca para Python la cual también la descargamos de su repositorio de github.

![imagen152](https://github.com/jmanday/Imagenes/blob/master/imagen152.png?raw=true)

![imagen153](https://github.com/jmanday/Imagenes/blob/master/imagen153.png?raw=true)


Cabe indicar que sólo muestro las imagenes de las instalaciones de las herramientas en una máquina virtual por evitar duplicar información, ya que he obviado poner también las de **Debian7** debido que es exacamente lo mismo.


<br>
<h3>Ejecutando la aplicación</h3>
Una vez instalados todos los servicios necesarios en las máquinas, pasamos a ejecutar la aplicación en cada una de ellas. Probando desde el anfitrión su correcto funcionamiento.

![imagen154](https://github.com/jmanday/Imagenes/blob/master/imagen154.png?raw=true)

![imagen156](https://github.com/jmanday/Imagenes/blob/master/imagen156.png?raw=true)

![imagen155](https://github.com/jmanday/Imagenes/blob/master/imagen155.png?raw=true)

![imagen157](https://github.com/jmanday/Imagenes/blob/master/imagen157.png?raw=true)

Al igual que comenté antes, para evitar duplicar y disminuir la cantidad de imagenes, sólo muestro las ejecuciones en las máquinas virtuales básicas tanto de **Ubuntu1310** como de **Debian7.**


<br>
<h3>Pruebas de carga</h3>
Para la realización de la pruebas he utilizado la herramienta **apache benchmark** por su sencillez y buen rendimiento a la hora de utilizarla. A cada una de las máquinas le he realizado la misma carga de trabajo:

<pre>
ab -n1000 -c100
</pre>

es decir, 1000 consultas con una concurrencia de 100 a la vez.

![imagen158](https://github.com/jmanday/Imagenes/blob/master/imagen158.png?raw=true)

![imagen159](https://github.com/jmanday/Imagenes/blob/master/imagen159.png?raw=true)

![imagen160](https://github.com/jmanday/Imagenes/blob/master/imagen160.png?raw=true)



<br>
<h3>Analizando los resultados</h3>
Una vez realizada todas las pruebas estos han sido los resultados obtenidos:
 
![imagen161](https://github.com/jmanday/Imagenes/blob/master/imagen161.png?raw=true)

Si analizamos la máquina basada en **Debian7** podemos ver que ofrece mejores resultados a menor prestaciones, la máquina mas básica es la que mejores tiempos ha obtenido, y así gradualmente con cada una de las modificaciones en las prestaciones que se realizó. 

Sin embargo en la máquina basada en **Ubuntu1310** no ocurre lo mismo, como por ejemplo las máquinas **Ubuntu1** y **Ubuntu2** las cuales sólo se diferencian en que esta última tiene el doble de memoria ram, el rendimiento es mejor en la que mayor memoria tiene, pero sin embargo si nos fijamos en las máquinas **Ubuntu3** y **Ubuntu4** que también sólo se diferencian en la memoria, la última tiene también el doble que la otra, en este caso no mejora el tiempo de respuesta, sino que lo empeora, cabe recordar que estas dos máquinas trabajan con 2 procesadores.

Si comparamos ambas máquinas, vemos como la máquina con **Debian7** obtiene incluso mejores resultados con la mitad de capacidad que la máquina con **Ubuntu1310**, algo que deja en evidencia a este último.


![grafica_debian](https://github.com/jmanday/Imagenes/blob/master/grafica_debian.png?raw=true)

![grafica_ubuntu](https://github.com/jmanday/Imagenes/blob/master/grafica_ubuntu.png?raw=true)


En estas gráficas muestro el porcentaje de peticiones atendidas en un determinado tiempo, en lo que también se cumple lo analizado anteriomente.


<br>
<h3>Conclusiones</h3>
Tras este estudio realizado se puede llegar a la conclusión de que no porque una máquina disponga de más soporte hardware va a prestar mejores servicios y responder mejor que otra que disponga de menos, sino que dependerá del sistema operativo sobre el que actúe. Hemos visto como si montamos nuestra aplicación sobre una máquina con **Ubuntu1310** a medida que vaya aumentando la capacidad de la misma (tanto en memoria como en procesadores), irán mejorando los tiempo de respuesta, directamente proporcional. Sin embargo cuando la aplicación ha sido montada sobe una máquina con **Debian7** no ha sido así, sino que da mejores resultados con capacidades inferiores (algo que viene muy bien para el tema económico €€.
Para acabar, como opinión personal y después de ver los resultados obtenidos me quedaría con **Debian7** para echar a rodar mi aplicación.
