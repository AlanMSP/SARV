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
 
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/Lectura.png)

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/Trafico.png)

### Ataques activos

Tambien están los ataques activos, que normalmente suceden despues de los ataques pasivos. A diferencia de los ataques pasivos, estos sí intentan alterar los recursos del sistema o afectar su funcionamiento. Los ataques activos son resultado de una "exploración" llevada a cabo con los resultados de múltiples ataques pasivos. Se puede intentar tomar ventaja de un proceso o función en especifico y comprometer la integridad del sistema.


![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/Modificacion.png)

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/Reenvio.png)

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/Suplantacion.png)

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/Interrupcion.png)

    
    
    

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
  
## Cifrado Feistel
  
Mensaje a cifrar: "OK"
<br>
  
"O": 01001111 
<br> 
  
"K": 01001011 
  
### Primera etapa

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/nivel1.png)
  
Para el cifrado Feistel se tiene como entrada un texto plano (de 16 bits para este ejemplo) y se generan 3 llaves aleatorias (K1, K2 y K3), las cuales se usarán posteriormente. 

En nuestra primera etapa se convierte nuestro texto plano a formato binario, se divide a la mitad nuestra cantidad de bits y se asignan nuestras mitades a dos variables. Una vez hecho esto, nuestra mitad derecha (R1) realiza una operación lógica XOR con nuestra primera llave generada (K1) y se guarda el resultado en una variable llamada "f1". Con f1 se realiza nuevamente una operación lógica XOR con la mitad izquierda (L1) y guardamos nuestro resultado en R2. Finalmente, en L2 se guardan los bits que teníamos en R1.

#### Función para generar llaves
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/Keycode.png)
  
#### Función para convertir texto plano a binario
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/TxtBincode.png)
  
#### Función XOR
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/XORcode.png)

#### Operaciones de nuestra primera etapa
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/nivel1ops.png)
  
### Segunda etapa
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/nivel2.png)

  
 Para la segunda etapa, recordemos que nuestra R1 de la primera etapa ha sido asignada como nuestra L2. Asimismo, nuestro R2 necesario para efectuar esta segunda etapa es el resultado del XOR realizado entre f1 y L1. Como primer paso, R2 es asignado como L3 para el siguiente paso, en segundo lugar se realiza un XOR entre ese mismo R2 y nuestra segunda llave aleatoria (K2). Guardando esté resultado y asignandolo como F2. Entre nustra nueva f2 y L2, se realiza un XOR para poder así obtener nuestro R3 para la tercer etapa.

#### Operaciones de nuestra segunda etapa
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/nivel2ops.png)

### Tercera etapa
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/nivel3.png)

  
En nuestra tercer etapa, se realiza un XOR entre R3 y nuestra tercera llave aleatoria (K3) y se guarda como F3. Éste mismo valor inicial de R3 es asignado a L4 para etapas posteriores. Por otro lado, se realiza un XOR entre L3 y F3, para así obtener cómo resultado nuestra última variante de R, R4. Tanto L4 como R4 ahora son cadenas de carácteres cifrados de 8 bits. 
  
#### Operaciones de nuestra tercera etapa
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/nivel3ops.png)
  
### Código completo
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/Feistelcode.png)
  
## Código de autentificación de mensajes (MAC)
  
En esta técnica de MAC, tanto el remitente como el destinatario comparten una llave, **_Key_**. Por medio de una función, se obtiene una clave secreta de nuestro mensaje y se utilizará para realizar otra función con nuestra llave previamente compartida. Esto generará nuestro código de autentificación (MAC), el cual se añadirá a nuestro mensaje. 
  
Una vez que nuestro mensaje ha sido enviado y posteriormente recibido, el destinatario debe realizar el mismo proceso para obtener el código de autentificación, usando las mismas funciones tanto para obtener nuestra clave secreta del mensaje como la que se utiliza con la llave. Ya que ha generado el código de autentificación, se compara con el que viene añadido al mensaje. Si este es igual, significa el mensaje se ha entregado sin modificaciones. En caso contrario, el mensaje ha sido alterado
  
### Código ejemplo en Python
  
En este ejemplo obtenemos nuestra clave secreta por medio de un conteo de ciertos caracteres del mensaje (comas, puntos y vocales), los cuales se suman para obtener un valor entero (**_clave)_**, el cual se convierte a binario en un formato de 8 bits (**_clave_bin_**). El cual realiza una operación XOR (**_exor_**) con nuestra llave de 8 bits generada aleatoriamente, **_Key_**. El resultado de dicha operación es nuestro código de autentificación (**_MAC_bin_**). Este código lo convertimos de binario a ASCII (**_MAC_**) y pegamos el caracter al final de nuestro mensaje a enviar. 
  
Para simular al destinatario, realizamos de nuevo las operaciones anteriores y generamos un código de autentificación en una variable diferente, **_MAC_binR_**. Realizamos una comparación entre los dos códigos generados, **_MAC_** y **_MAC_binR_**. Si estos son iguales, se despliega un leyenda de que nuestro mensaje ha sido recibido sin modificaciones y se muestra el mensaje original sin el código de autentificación. 
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/MAC.png)
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/MACejemplo.png)

## Función HASH para la autentificación de mensajes
  
 Por HASH, se refiere a un proceso criptográfico que puede ser usado para validar la autenticidad e integridad de varios tipos de datos. Es muy usado en sistemas de autenticación para evitar almacenar contraseñas simples en las bases de datos, aunque tambien es usado para validar los contenidos de un archivo, documentos u otros tipos de datos. El uso incorrecto de funciones hash puede resultar en vulnerabilidades importantes pero en sí, no usar esta función para asegurar datos sensibles es mucho peor.
  
La función HASH realiza un _resumen_ de nuestro mensaje a enviar (*_valor secreto_*). Esta clave secreta  realiza la operación lógica XOR con una llave compartida previamente con el destinatario y el resultado de la operación se envía junto con el mensaje para la autenticidad de éste.

Una vez que nuestro mensaje ha sido enviado y recibido, el destinatario debe realizar dos operaciones: Realizar un XOR entre la llave compartida y el HASH recibido, y realizar el HASH del mensaje original. Una vez obtenidos ambos valores, se comparan y, si estos son iguales, significa que el origen del mensaje ha sido autentificado. 

### Ejemplo de función HASH en EXCEL
  
El proceso para poder generar nuestro resultado, es en primer lugar, designar nuestro mensaje plano. En este caso, hemos elegido la palabra MUNDO y necesitamos descomponer sus carácteres en valores de 8 bits, para así poder manipular sus contenidos con operaciones XOR. Cómo primer paso en nuestro HASH, la etapa 1 del mismo siempre se inicializa en 0, para así poder realizar nuestro primer XOR entre Hash1 y B1 (letra M de MUNDO en binario) para así poder obtener nuestro H2. Acto seguido, a H2 se le hace una rotación de 1 bit a la izquierda, y con esta rotación aplicada podemos obtener H2-2. Este valor se usa en un XOR con la siguiente cadena de carácteres correspondientes a la letra U de MUNDO (B2). El resultado de dicha operación se designa como H3 y el proceso se repite las veces que sea necesario, dependiendo del número de bits que tenga el mensaje.
  
Una vez recorridos todos los bloques de nuestro texto plano separado, se obtiene un valor de 8 bits (H6), el cual sería nuestro HAS. En este método convencional, el HASH se codifica realizando una operación lógica XOR con nuestra llave compartida previamente y el resultado se añade a nuestro mensaje a enviar. 
  
![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/HASH.png)
  
## Función HASH segura SHA-1
  
### Procesamiento SHA-1 de un bloque de 512 bits
    
  Este algoritmo toma como entrada un mensaje con una longitud máxima menor a 2^64 bits y produce como salida un resumen de ese mensaje con longitud de 160 bits. Este procesamiento se efectúa en bloques de 512 bits y se puede desglosar en los siguientes pasos:

### Paso 1 
Adición de bits de relleno: El mensaje original es rellenado para que su longitud sea congruente, con 448 módulo 512. Esto significa que la longitud del mensaje relleno es 64 bits menos que un múltiplo de 512 bits. Este relleno es añadido aunque el mensaje concuerde con la longitud deseada. De esta forma el número d e bits que se utilizaron para rellenar se encuentra entre 1 y 512. El relleno está conformado por un único bit 1 seguido del número necesario de bits.


### Paso 2   
Añadir longitud: Se añade un bloque de 64 bits al mensaje original, este bloque se trata como un entero sin signo de 64 bits y contiene la longitud del mensaje original antes del relleno. Esta inclusión de un valor de longitud brinda protección contra un ataque conocido cómo “ataque de relleno”.

El resultado de estos dos primeros pasos nos brinda un mensaje que es un entero múltiple de 512 bits de longitud.

### Paso 3 
Inicializar el buffer MD: Se utiliza un buffer de 160 bits para tener resultados intermedios y finales de la función HASH. Este buffer puede representarse como cinco registros de 32 bits (A, B, C, D, E). Estos registros se inicializaban a los siguientes enteros de 32 bits (valores hexadecimales):


A = 67452301
B = EFCDAB89
C = 98BADCFE
D = 10325476
E = C3D2E1F0

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/SHA-1.png)

### Paso 4 
Procesar el mensaje en bloques de 512 bits (16 palabras). El módulo principal del algoritmo es llamado FUNCIÓN DE COMPRESIÓN, esta función está conformada por cuatro etapas de procesamiento de 20 pasos. Estas etapas funcionan de una manera muy similar pero cada una utiliza una función lógica primitiva diferente. (f1, f2, f3, f4)

Cada etapa toma como entrada el bloque de 512 bits que se está procesando (Yq) y el valor de ABCDE del buffer de 160 bits y actualiza los contenidos del buffer. 

También es importante mencionar que en cada etapa se utiliza una constante adicional (Kt) donde 0 < t < 79 especifica uno de los 80 pasos a lo largo de las cinco etapas. En realidad sólo se usan cuatro constantes distintas, a continuación, se muestran los valores en decimal y hexadecimal:

Número de paso            Hexadecimal            toma parte entera de:
<li>0 < t < 19                Kt = 5A827999          2^30 x sqrt2 </li>
<li>20 < t < 39               Kt = 6ED9EBA1          2^30 x sqrt3 </li>
<li>40 < t <  59              Kt = 8F1BBCDC          2^30 x sqrt5 </li>
<li>60 < t < 79               Kt = CA62C1D6          2^30 x sqrt10 </li>

<br> 

La salida de la cuarta etapa (paso no. 80) es añadida a la entrada del primer paso en todo el proceso (CVq) para así generar (CVq+1). La suma se hace de manera independiente para cada una de las cinco palabras en el buffer con cada una de las palabras que corresponden en CVq, utilizando la suma módulo 2^32.

### Paso 5 
Una vez que la totalidad de los bloques L de 512 bits han sido procesados, la salida del último estado (el L-ésimo) es el resumen del mensaje de 160 bits. El algoritmo tiene la propiedad por la cual cada bit del código HASH es una función de cada bit de la entrada. La repetición compleja de la función básica ft produce resultados con un grado de aleatoriedad muy bueno, es decir, es poco probable que dos mensajes tengan el mismo código HASH, la dificultad de dar con dos mensajes con el mismo resumen es del orden de 2^80, mientras que la dificultad de encontrar un mensaje con un resumen dado es del orden de 2^160 operaciones.

## Algoritmo de cifrado de clave pública RSA

### Código completo en pyhton

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/RSAcode.png)

### Ejemplo

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/RSAexample.png)


## GPG - Cifrando y descifrando archivos 

### ¿Cómo instalar?

PGP es una herramienta de cifrado y firmas digitales desarrollado por Werner Koch, que viene a ser un reemplazo del PGP pero con la principal diferencia que es software libre licenciado bajo la GPL. Su versión más reciente puede ser descargada desde la consola de comandos de cualquier distribución Linux con el siguiente comando: 

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/GPG1.PNG)

De manera normal, nosotros podemos generar un archivo (de cualquier tipo), en este caso crearemos un archivo .txt en nuestro directorio actual y procederemos a cifrarlo:

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/GPG3.PNG)

Acto seguido, nos pedirá que ingresemos una "passphrase". Es importante hacer enfásis en que si esta frase es olvidada, el archivo no podrá ser descifrado. Esta frase se utilizará de la misma manera para poder descifrar los contenidos del archivo.

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/GPG4.PNG)

Al ingresar la frase, junto con su confirmación, la versión del archivo cifrado se generará en el mismo directorio donde fue ejecutado el comando: 

![image](https://raw.githubusercontent.com/AlanMSP/SARV/main/GPG5.PNG)

Si queremos visualizar el contenido de dicho archivo nos daremos cuenta que ya están cifrados y solo podrá ser descrifrado con el comando "gpg -d [ARCHIVO]" y la frase inicial que fue utilizada para su cifrado.

## Kerberos 

### ¿Qué es Kerberos?

En un sistema de computo, los usuarios validan sus identidades usando contraseñas, aunque eso es sencillo de implementar, siempre tendrá una falla de seguridad muy importante, si un hacker roba o crackea la contraseña, es muy fácil suplantar la identidad de la persona en cuestión. Los intrusos se logean al sistema como el usuario real y el sistema queda abierto a un ataque directo. 

Kerberos es un protocolo de seguridad para aplicaciones cliente/servidor, este protocolo se basa en una combinación de llaves privadas de encriptación y tickets de acceso para verificar de manera segura la identidad del usuario. La principal función proteger las credenciales de los usuarios de ataques. Este protocolo protege las claves de secciones de la red inseguras, aún durante la autenticación de usuarios.


Las principales fortalezas de Kerberos:

- Las contraseñas de texto plano jamás son enviadas a través de una red insegura.
- Todos los inicios de sesión cuentan con tres etapas de autenticación.
- La encriptación protege todas las llaves de acceso y los tickets.
- La autenticación es mutua, así que tanto los usuarios como los proveedores de un servicio están a salvo de ataques.

### Los tres componentes de Kerberos

Toda aplicación de Kerberos cuenta con un centro de distribución de llaves. Este centro actúa como un servicio de autenticación externo confiable y opera desde el servidor Kerberos y consta de los siguientes 3 componentes:

- Servidor de Autenticación (AS): Este servidor realiza una autenticación inicial cuando el usuario intenta acceder a un servicio. Se inicia el protocolo cuándo el usuario hcae una petición de acceso, esta solicitud está parcialmente encriptada con una llave secreta, la contraseña del usuario. Esta clave es un secreto compartido entre el servidor de autenticación y el usuario. En caso de que el servidor no pueda descifrar el mensaje, será porque el usuario no introdujo correctamente su contraseña. Si la solicitud es desencriptada, el servidor de autenticación genera un ticket-granting ticket (TGT, ticket para brindar otro ticket) y lo encripta con la llave privada del Servidor de Conseción de Tickets. Esta llave es un secreto compartido entre el Servidor de Autenticación y el Servidor de Conseción de Tickets.

Un TGT contiene una llave de sesión cliente/TGS, una fecha de expiración y la dirección IP del cliente. La dirección IP protege la conexión de ataques ubicados en algún punto medio de la conexión. Una vez que este TGT es generado, el AS lo envía al usuario.

- Servidor de Conseción de Tickets (TGS): Este servidor conecta al usuario con el servicio al que intenta acceder. El usuario envía el TGT al TGS, si este ticket es válido y el usuario tiene los permisos para acceder al servicio, el TGS genera un ticket de servicio. Un ticket de servicio contiene el ID del usuario, su dirección en la red, periodo de validez y una llave de sesión cliente/servidor. El ticket de servicio es encriptado con una llave secreta compartida con el servidor de servicios.

- Servidor Kerberos (Base de Datos): Esta base de datos almacena los ID's y contraseñas de los usuarios verificados.

![image](https://github.com/AlanMSP/SARV/blob/main/Imagenes%20-%20Seguridad%20de%20redes(1).jpg)

### ¿Cuáles son los pasos en la autenticación de Kerberos?

El proceso de autenticación de Kerberos tiene distintas etapas:

1.- El usuario envía una solicitud al AS, cuando el AS recibe la solicitud, busca por la contraseña en la base de datos de Kerberos que corresponde al usuario, si el usuario introdujo correctamente la contraseña, el AS desencripta la solicitud.

2.- El AS genera un TGT, despues de verificar al usuario, el AS envía un TGT.

3.- El usuario hace una solicitud con su TGT al TGS, además de eso, también especifica la razón por la cual quiere acceder al servidor (por ejemplo, leer un archivo), El TGS desencripta el ticket con la llave compartida con el AS.

4.- El TGS genera un ticket de servicio y se lo envía al usuario, siempre y cuando el TGT haya sido válido.
Estos procesos se llevan a cabo en una implementación Kerberos 

5.- El usuario envía el ticket de servicio al servidor donde se encuentra el archivo, el servidor desencripta el mensaje con una llave secreta compartida con TGS.

6.- El usuario lee el documento: Si las llaves secretas concuerdan, el servidor de archivos permite al usuario abrir el documento, el ticket de servicio determina cuanto tiempo el usuairo tiene acceso al archivo, una vez que éste expira, el usuario necesita volver a pasar por todo el proceso de solicitar acceso a Kerberos.
