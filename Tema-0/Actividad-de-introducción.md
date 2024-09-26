# Actividad de presentación de la asignatura 

# Daniel Damota Maldonado 

 

Visualiza los siguientes videos y responde a las cuestiones planteadas a continuación 

<br><br>

## Actividad 0.1 - HTTP Introduction

https://www.youtube.com/watch?v=eesqK59rhGA 

https://www.youtube.com/watch?v=DuSURHrZG6I 

<br><br>

 

¿Quién, dónde y cuándo se crea el primer servidor web? 

El primer servidor web fue creado por Tim Berners-Lee, un científico británico del CERN (Organización Europea para la Investigación Nuclear) en Suiza. Fue lanzado el 6 de agosto de 1991, y se considera el nacimiento oficial de la World Wide Web (WWW). 

<br><br>

<u>¿Qué es pila de protocolos usados por http?</u>

La pila de protocolos usada por HTTP (Hypertext Transfer Protocol) se refiere a los distintos niveles o capas de protocolos de red que permiten la comunicación en la web. 

<br><br>

¿Componentes de una URL? 


Un URL se compone de los siguientes elementos: 

<br>

- Esquema/Protocolo: Indica el protocolo a usar (e.g., http://, https://). <br>

- Dominio/Host: El nombre del servidor o IP (e.g., www.ejemplo.com). <br>

- Puerto (opcional): Especifica el puerto (e.g., :8080). <br>

- Ruta/Path: La ubicación del recurso en el servidor (e.g., /articulos/). <br>

- Consulta/Query (opcional): Parámetros adicionales (e.g., ?id=123). <br>

- Fragmento (opcional): Un ancla dentro de la página (e.g., #seccion). <br>

 
<br><br>
 

## ¿Pasos en la recuperación de una página web mediante HTTP? 

 <br>

- Resolución DNS: El navegador convierte el dominio en una dirección IP. 

 <br>

- Conexión TCP: Se establece una conexión entre el navegador y el servidor. 

 <br>

- Solicitud HTTP: El navegador envía una solicitud HTTP al servidor. 

 <br>

- Respuesta HTTP: El servidor responde con el contenido de la página (HTML, 

  CSS, etc.). 

 <br>

- Renderizado: El navegador interpreta y muestra la página web. 

<br><br>

Diferencia entre páginas dinámicas y estáticas 

<br>

Páginas estáticas: 

 

El contenido no cambia a menos que se edite manualmente el archivo. 

 

Están predefinidas en archivos HTML que el servidor entrega tal cual al navegador. 

 

Ejemplo: un sitio web de una empresa con información fija 

 

Páginas dinámicas: 

 

El contenido se genera en tiempo real, basado en solicitudes del usuario o datos del servidor. 

 

Utilizan lenguajes de programación como PHP, Python o JavaScript para generar el HTML dinámicamente. 

 

Ejemplo: una red social donde el contenido cambia según el usuario que accede. 

 

 

¿Cómo usar telnet para acceder a un servidor web? 

(solución en actividad 0.3) 

 

 

 

Request. Métodos principales 

 

Métodos: GET (envía recursos) y POST (envía datos para que sean procesados), PUT, HEAD y DELETE. 

 

Response. Códigos:  

 

Códigos con formato 1xx: Respuestas informativas. Indica que la petición ha sido recibida y se está procesando. 

 

Códigos con formato 2xx: Respuestas correctas. Indica que la petición ha sido procesada correctamente. 

 

Códigos con formato 3xx: Respuestas de redirección. Indica que el cliente necesita realizar más acciones para finalizar la petición. 

Códigos con formato 4xx: Errores causados por el cliente. Indica que ha habido un error en el procesado de la petición a causa de que el cliente ha hecho algo mal. 

 

Códigos con formato 5xx: Errores causados por el servidor. Indica que ha habido un error en el procesado de la petición a causa de un fallo en el servidor. 

 

 

Content type. Tipos principales:  

 

text: Indica que el contenido es texto plano. Ejemplos de subtipos: html, xml 

 

multipart: Indica que tiene múltiples partes de datos independientes. Ejemplos de subtipos: form-data, digest 

 

message: Para encapsular un mensaje existente. Por ejemplo cuando queremos responder a un mensaje de correo incorporando el mensaje origen. Ejemplos de subtipos: partial, rfc822 

 

image: Indica que es una imagen. Ej de subtipos: png, gif 

 

audio: Indica que es un audio. Ejemplos de subtipos: mp3, 32kadpcm 

 

video: Indica que es un video. Ejemplos de subtipos: mpeg, avi 

 

application: Indica que se trata de datos de aplicación los cuales pueden ser binarios. Ejemplos de subtipos: json, pdf 

 

 

 

 

 

 

 

 

 

Actividad 0.2 - UDP and TCP: Comparison of Transport Protocols 

https://www.youtube.com/watch?v=Vdc8TCESIg8 

 

Diferencias entre udp y tcp (min 2:46 y 4:15) 

 

Conexión: 

 

TCP: Es un protocolo orientado a la conexión. Establece una conexión antes de enviar datos. 

 

UDP: Es un protocolo sin conexión. Envía datos sin establecer una conexión previa. 

 

Fiabilidad: 

 

TCP: Garantiza la entrega de paquetes y el orden correcto. Realiza corrección de errores. 

 

UDP: No garantiza la entrega ni el orden. Es más rápido, pero menos fiable. 

 

 

¿Qué aplicaciones usan tcp?  

 

HTTP, IMAC, POP, SMTP 

 

¿Qué aplicaciones usan udp?  

 

DNS, SNMP 

 

¿Qué capa almacena el puerto?  

 

Capa de Transporte: TCP y UDP utilizan números de puerto para identificar aplicaciones específicas. 

 

¿Qué capa almacena la dirección IP? 

 

Capa de Red: La dirección IP se utiliza para identificar dispositivos en una red. 

 

 

 

¿Qué es three-way handshake? 

 

El three-way handshake (apretón de manos en tres pasos) es el proceso que utiliza el protocolo TCP para establecer una conexión confiable entre un cliente y un servidor antes de comenzar a intercambiar datos. Este mecanismo garantiza que ambas partes estén listas para la comunicación. 

 

 

 

 

 

 

Actividad 0.3 - Práctica telnet/http 

https://www.youtube.com/watch?v=xpBpGC08f4Q&t=189s 

http://www.profesordeinformatica.com/servicios/http/telnet 

Lee el artículo y prueba los ejemplos sugeridos en él. 

 

Nota: Si usamos Windows 10, tenemos que activar “telnet” 

http://www.lawebdelprogramador.com/foros/Windows-10/1510815-Como-activar-Telnet-en-Windows-10.html 

 

 

Uso de comando telnet www.google.com 80 y luego GET / HTTP/1.1 para obtener el código de la página web: 
