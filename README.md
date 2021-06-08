# Seguridad y Administración de Redes - Verano

<br>

###  1.1. La arquitectura de seguridad OSI <br>
<br>
La importancia del modelo OSI en este enfoque se debe a la naturaleza de las amenazas y ataques, así como el proceso que siguen los datos al momento de ser enviados/recibidos. Es de crucial importancia tener en cuenta cada capa de este modelo y las amenazas que se presentan en cada escenario.
<br>
<br>

###   1.2. Ataques a la seguridad
<br>
Los ataques a la seguridad tienen cómo característica principal ser un intento de vulnerar al proceso "normal" de un sistema o de información. Asímismo, se dan en forma de escucha o de observación no autorizadas de las transmisiones. Se realiza el atentado y no hay mucha (si no es que ninguna) evidencia de lo ocurrido. La obtención de contenidos de mensajes se puede ejemplificar muy fácilmente, un mensaje, una llamada telefónica o un archivo pueden contener información confidencial, es crucial evitar que un oponente conozca dichos contenidos.
  
A este tipo de ataques se les denominan con dos términos, activos y pasivos. Los pasivos se enfocan en observar o analizar cierta transimisión, pero no afectan a los recursos de la misma.

### Ataques pasivos
 
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/1.png)

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/2.png)

### Ataques activos

Tambien están los ataques activos, que normalmente suceden despues de los ataques pasivos. A diferencia de los ataques pasivos, estos sí intentan alterar los recursos del sistema o afectar su funcionamiento. Los ataques activos son resultado de una "exploración" llevada a cabo con los resultados de múltiples ataques pasivos. Se puede intentar tomar ventaja de un proceso o función en especifico y comprometer la integridad del sistema.


![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/3.png)

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/4.png)

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/5.png)

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/6.png)

    
    
    

###   1.3. Servicios de seguridad
<br>

X.800 es una recomendación de las características básicas que deben ser consideradas cuando se quiere conectar una computadora con otras. No es una especificación de implementación, sino una descripción de los servicios de seguridad básicos que pueden ser aplicados cuando es necesario proteger la comunicación entre sistemas.
<br>

El RFC 2828 trata de las definiciones de un conjunto de abreviaciones, términos yrecomendaciones para el uso de una terminología relacionada a la seguridad de los sistemas deinformación.
<br> 

En base a la vulnerabilidad de los datos a compartir, las consecuencias en caso de que la información se comprometa y el costo de aplicación de un mecanismo de seguridad se implementan (dentro del mecanismo) una serie de servicios de seguridad que tienen como tarea principal brindarle una protección especial a los recursos del sistema. 
<br>
<br>
Algunos ejemplos serían:
<br>
<ol>
<li>Autentificación: La seguridad de que la entidad en cuestión es quién dice ser.</li>
<li>Control de Acceso: Una serie de reglas aplicadas a diferentes instancias del sistema, para evitar el uso o explotación de una característica que podría resultar en un acceso no deseado.</li>
<li>Confidencialidad de los Datos: La protección de los datos contra una revelación no autorizada.</li>
<li>Integridad de los datos: La seguridad de que la información que se envía/recibe no ha sufrido alguna modificación en ningún punto de su ruta. </li>
<li>No repudio: Proporciona protección contra la interrupción en la totalidad de la ruta llevada a cabo. En otras palabras, evita que ninguna entidad en cuestión puedan negar la transmisión.</li>
</ol>
<br>
<br>

###   1.4. Mecanismos de Seguridad

1.- Mecanismos especificos de seguridad

<br>
Este tipo de funcionalidades pueden ser implementadas en la capa del modelo OSI más adecuadas.
<br>
<br>
<li>Crifrado: El uso de algoritmos para convertir la información  a inteligible y legible, gracias al resultado del algoritmo.
<li>Firma digital: Datos adjutos a una unidad de datos para simular la función de una llave.
<li>Control de acceso: Mecanismos que refuerzan los derechos de un usuario.
<li>Integridad de los datos: Mecanismos empleados para confirmar la falta de modificaciones no autorizadas al archivo base.
<li>Intercambio de autentificación: Mecanismo diseñado para comprobar la identidad de una entidad gracias al intercambio de información.
<li>Relleno de tráfico: Se refiere a la inserción de bits en un flujo de datos para frustrar los intentos de análisis de tráfico.
<li>Control de enrutamiento: Permite personalizar la ruta en la que se envían los datos, para protección preventiva o correctiva.
<li>Notarización: El uso de una tercera parte confiable que funge como asegurador de determinadas propiedades de un intercambio de datos.
<br>
<br>
2.- Mecanismos generales de seguridad

<br>
Este tipo de funcionalidades no son especificas de alguna capa del modelo OSI o sistema de seguridad en particular:
<br>
<br>
<li>Funcionalidad fiable: La que se considera correcta con respecto a algunos criterios
<li>Etiquetas de seguridad: la marca asociada a un recurso que designa los atributos de seguridad de ese recurso 
<li>Detección de acciones: Detección de acciones relacionadas con la seguridad
<li>Informe para la auditoría de seguridad: Recopilación de datos para facilitar una auditoría de seguridad.
<li>Recuperación de seguridad: Maneja las peticiones de los mecanismos y lleva a cabo acciones de recuperación.

<br>
<br>

###   1.5. Un Modelo de Seguridad en Redes
<br>

La idea de una acción de compartir información por la red significa que siempre van a haber dos interlocutores, receptor y remitente, gracias al protocolo TCP/IP se establece un canal de información o ruta óptima.

<br>
Al momento de tener la necesidad de proteger información de cualquier persona que no sean los dos interlocutores iniciales, se deben desarrollar técnicas de seguridad, que siempre cuentan con dos carácteristicas principales:
<br>
<br>
<li>Una transformación relacionada a la seguridad para que, en caso de que el mensaje sea interceptado, el contenido no sea accesible.
<li>Algún tipo de información secreta compartida por los interlocutores exclusivamente.
<br>
<br>
Este modelo nos permite identificar 4 puntos cruciales para el diseño de un    servicio de seguridad particular:
<ol>
<li>Diseñar un algoritmo que resulte en la transformación de la información.
<li>Generar información confidencial para ser utilizada mediante el algoritmo.
<li>Desarrollar métodos de distribución eficientes.
<li>Especificar un protocolo e instruir a los locutores del mismo para su correcta aplicación.
<br>
<br>
</ol>

No se puede hablar de seguridad sin mencionar las intrusiones que consisten en introducir piezas de hardware dañinas para el sistema. Se tratan de las siguientes amenazas potenciales:
<br>
<br>
<li> Amenazas al acceso de información: captura o alteración de datos por parte de usuarios externos.
<li> Amenazas al servicio: explotación de fallos del servicio para impedir el uso por parte de usuarios legítimos.   
<br>
<br>

### 1.6 Estándares de internet y la Sociedad Internet.
<br>
 
La Sociedad Internet es una organización que se encarga del funcionamiento y estandarización de internet. Dentro de este ámbito existen 3 organizaciones responsables del desarrollo y publicación de los estándares: 
<br>

<li> IAB: responsable de definir la arquitectura general de internet.
<li> IETF: encargada del desarrollo e ingeniería de protocolos en internet.
<li> IESG: responsable de la gestión técnica de las actividades de la IETF y del proceso de estándares de internet.
<br>
<br>
  
#### El proceso de estandarización
<br>
  
La IETF crea Borradores de Internet, los cuales son borradores de documentos de especificaciones en desarrollo que se mantendrán hasta 6 meses en revisión. Después de ese periodo, la IESG es quien determinará si el borrador se publicará como RFC, y es la IETF quien hará o no la publicación. Para que se aprueben como estándares, las especificaciones deben cumplir con los siguientes requisitos: 
<br>
  
<li> Ser estable y comprensible.
<li> Ser técnicamente competente.
<li> Tener implementaciones múltiples, independientes e interoperativas con una experiencia operativa sustancial.
<li> Tener apoyo público significativo.
<li> Ser reconocidamente útil en algunas o en todas las partes de internet.
<br>
<br>
  
#### Categorías de estándares de internet
<br>
  
Se dividen en dos categorias:
<br>
  
<li> Especificación técnica: define un protocolo, servicio, procedimiento, convención o formato.
<li> Informe de aplicabilidad: especifica cómo y en qué circunstancias una o más especificaciones técnicas pueden aplicarse para posibilitar una determinada capacidad de Internet.
<br>
<br>
 
#### Otros tipos de RFC
<br>
  
Existen algunos RFC que no se convierten en estándares de internet, como el BCP, los RFC experimentales y los RFC informativos. 
