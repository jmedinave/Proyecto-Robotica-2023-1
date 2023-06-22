# Proyecto-Robotica-2023-1 UNAL
En este repositorio se realiza una descripción de todo el proceso de diseño y el cumplimiento de los objetivos del proyecto propuesto en la asignatura de robotica 2023-1 UNAL: 

### Integrantes: 
![image](https://github.com/jmedinave/Proyecto-Robotica-2023-1/assets/49196705/457dc984-36b6-4689-b432-bc3989945ab2)




### Objetivo General
Realizar un análisis comparativo entre el tiempo promedio de alistamiento manual y el tiempo de alistamiento utilizando un brazo manipulador industrial en un proceso de preparación y ubicación de contenedores y piezas en una estantería. Se busca determinar la eficiencia y rapidez de la automatización en comparación con el proceso manual, considerando las diferentes combinaciones de piezas y posiciones en la estantería.

### proceso de Alistamiento.
<ul>
    <li><strong>El proceso de alistamiento:</strong> Se debe tomar el contenedor (balde) del extremo de la banda transportadora y ubicarlo en un lugar de alistamiento. Se deben tomar 3 piezas distintas de la estanter&iacute;a de madera y ubicarlas en el balde. El pedido listo (balde+piezas) debe ser ubicado de regreso sobre la banda transportadora.</li>
  
</ul>

<p><br></p>
<ul>
    <li><strong>Alistamiento de la estanter&iacute;a:</strong> La estanter&iacute;a de madera tiene 6 posiciones (A,B,C,D,E,F), se deben ubicar 6 piezas distintas en cada posici&oacute;n de la estanter&iacute;a. El tama&ntilde;o, forma, material y dem&aacute;s caracter&iacute;sticas pueden ser ajustadas de acuerdo a la herramienta dise&ntilde;ada.</li>


</ul>

![image](https://github.com/jmedinave/Proyecto-Robotica-2023-1/assets/49196705/f61038ea-55e5-4c19-98d6-fc0cbf26cb3d)


<p><br></p>
<ul>
    <li><strong>Posicionamiento de los elementos:</strong> Tanto la estanter&iacute;a como las piezas en cada una de las 6 posiciones pueden ser posicionadas al espacio de trabajo diestro del manipulador, todo ajuste se debe realizar con el brazo inm&oacute;vil y solamente al inicio del proceso.</li>


</ul>

![image](https://github.com/jmedinave/Proyecto-Robotica-2023-1/assets/49196705/4f0bbebf-9837-4f42-962b-5411707e38c5)


<p><br></p>
<ul>
    <li><strong>An&aacute;lisis de tiempo manual:</strong> Se debe realizar pruebas de trabajo manual utilizando una sola mano, donde se pueda identificar el tiempo promedio de alistamiento manual para las combinaciones estudiadas. Para ello, se graba en video el intento a mano:  </li>
</ul>

#### Intento a mano:
<p>
    PULSAR IMAGEN PARA VIDEO:</p>
<p><br></p>

[![Alt text](https://img.youtube.com/vi/vFiJtqvFv7U/0.jpg)](https://www.youtube.com/watch?v=vFiJtqvFv7U)

### Diseño de la herramienta.
En este apartado, se realiza una descripción del proceso de diseño así como de sus requisitos de diseño.
<p><br></p>
<p>&Eacute;l porta herramientas, tiene un principal objetivo, el cual es sostener las dos herramientas auxiliares con las que se cuentan para este proyecto. Estas son el <strong>gancho</strong> para sostener y trasladar el balde y, por otra parte, la <strong>ventosa neum&aacute;tica</strong>. La cual tendr&aacute; funci&oacute;n de &quot;gripper&quot; el cual sostendr&aacute; y trasladara las piezas o fichas para depositarlas en el balde.</p>

#### Requisitos de diseño:
<ul>
    <li>El portaherramientas debe sostener la ventosa y el gancho.</li>
    <li>Debe ser ligero.</li>
    <li>Debe tener un tama&ntilde;o reducido y suficientemente robusto. El portaherramientas debe ser lo suficientemente robusto para soportar el peso de las herramientas y las piezas y tener seguridad que no se romper&aacute; con facilidad. Del mismo modo, debe ser de tama&ntilde;o reducido para obtener m&aacute;s maniobrabilidad en el manipulador.</li>
    <li>Debe ir acoplado al soporte que se atornilla al robot. Este soporte se dise&ntilde;&oacute; en laboratorio No&deg; 1.</li>
</ul>

![image](https://github.com/jmedinave/Proyecto-Robotica-2023-1/assets/49196705/96ef461c-a50a-4fde-95e4-a3234a226a01)

A continuación las medidas generales, En los archivos adjuntos podra encontrar el plano de la pieza y el archivo CAD.
![image](https://github.com/jmedinave/Proyecto-Robotica-2023-1/assets/49196705/1de2328c-c29c-472f-a89b-26366b54cc81)

![image](https://github.com/jmedinave/Proyecto-Robotica-2023-1/assets/49196705/361f08d1-aa19-41c2-8062-c3255894701d)



###  Consideraciones:
El brazo debe sujetar cada pieza y ensamblarla en el orden y orientación correcta, las piezas deben encajar sobre
los pasadores de la base de ensamble y las piezas anteriores.
Realice pruebas de succión para validar que las 6 piezas pueden ser sujetadas con firmeza por las ventosas, ajuste
cualquier tamaño que considere necesario.
La ubicación de la estantería y la banda transportadora deben estar enlazadas a objetos de trabajo que permitan
su ajuste en la práctica. Se recomienda que el modelado de la herramienta esté ajustado a las dimensiones reales
de la construcción.
El Balde solo debe ser tomado utilizando el gancho metálico, no se deben realizar cambios permanentes al balde ni
al gancho. Es posible que se quiera dejar fija la manija del balde, se sugiere algún método de sujeción temporal.
Las velocidades, zonas de aproximación y otros parámetros de movimiento quedan a discreción de cada equipo de
trabajo, según lo visto en clase, condiciones de trabajo seguro y las indicaciones del docente en el laboratorio.
Es probable que el limite de velocidad del proceso esté relacionado con la dinámica del balde, la manija y el gancho,
identifique los limites dinámicos de la operación.


### Proceso automatizado:

<p>Se deben tomar 3 de las 6 piezas de la estanter&iacute;a para ser ubicadas en el balde, se deben probar al menos 4 (ejemplo B+D+F) combinaciones de piezas para establecer un promedio de alistamiento.</p>
<p>El proceso de alistamiento debe iniciar al presionar un bot&oacute;n del tablero por cada combinaci&oacute;n (entrada digital) y se debe encender una luz de indicaci&oacute;n en el tablero (salida digital) una vez finalizado el proceso, el brazo debe iniciar y terminar el proceso en la posici&oacute;n de Home de laboratorio (0,0,0,0,0,0).</p>
<p><br></p>



#### 1. Simulación:



<p>
    PULSAR IMAGEN PARA VIDEO:</p>
<p><br></p>

[![Alt text](https://img.youtube.com/vi/6KjO7En3JUI/0.jpg)](https://www.youtube.com/watch?v=6KjO7En3JUI)

#### 2. Resultados:


##### Combinación 1:
<p>
    PULSAR IMAGEN PARA VIDEO:</p>
<p><br></p>

[![Alt text](https://img.youtube.com/vi/-A1WfqrAXSg/0.jpg)](https://www.youtube.com/watch?v=-A1WfqrAXSg)

##### Combinación 2:
<p>
    PULSAR IMAGEN PARA VIDEO:</p>
<p><br></p>

[![Alt text](https://img.youtube.com/vi/lJE3ixzhj00/0.jpg)](https://www.youtube.com/watch?v=lJE3ixzhj00)

##### Combinación 3:
<p>
    PULSAR IMAGEN PARA VIDEO:</p>
<p><br></p>

[![Alt text](https://img.youtube.com/vi/T1-0djskq6s/0.jpg)](https://www.youtube.com/watch?v=T1-0djskq6s)

##### Combinación 4:
<p>
    PULSAR IMAGEN PARA VIDEO:</p>
<p><br></p>

[![Alt text](https://img.youtube.com/vi/SksNIu4N36M/0.jpg)](https://www.youtube.com/watch?v=SksNIu4N36M)

##### Incremento en la velocidad:
<p>
    PULSAR IMAGEN PARA VIDEO:</p>
<p><br></p>

[![Alt text](https://img.youtube.com/vi/9GWeYfzFmc0/0.jpg)](https://www.youtube.com/watch?v=9GWeYfzFmc0)



### Conclusiones:

- Robots industriales como el IRB140, gracias a su exactitud, permiten realizar tareas que requieren una alta precisión y exactitud.Esto los hace útiles para, por ejemplo, el ensamble de herramientas. A tal punto que pueden llegar a ensamblar un mecanismo que funciona, como el gripper en este caso.
  
- Un Robot industrial aumenta su funcionalidad por medio de actuadores secundarios, en este caso la ventosa y su sistema de succión.
  
- Debido a la exactitud con la que operan los robots industriales, es necesario tener un dimensionamiento de precisión de las herramientas que se le adecuaran, más aún en aplicaciones de alta precisión.
