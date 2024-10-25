
<p align="center">
  <img src="https://github.com/user-attachments/assets/92b13dd5-01d7-4f83-8bb6-e218dfb11235" alt="Descripción de la imagen"/>
</p>

# Actividad de presentación de la asignatura 

# Daniel Damota Maldonado 

Visualiza los siguientes videos y responde a las cuestiones planteadas a continuación 

<br>

## Actividad 0.1 - HTTP Introduction

https://www.youtube.com/watch?v=eesqK59rhGA 

https://www.youtube.com/watch?v=DuSURHrZG6I 

<br><br>

### ¿Quién, dónde y cuándo se crea el primer servidor web? 

El primer servidor web fue creado por Tim Berners-Lee, un científico británico del CERN (Organización Europea para la Investigación Nuclear) en Suiza. Fue lanzado el 6 de agosto de 1991, y se considera el nacimiento oficial de la World Wide Web (WWW). 

<br><br>

### ¿Qué es pila de protocolos usados por http?

La pila de protocolos usada por HTTP (Hypertext Transfer Protocol) se refiere a los distintos niveles o capas de protocolos de red que permiten la comunicación en la web. 

<br><br>

### ¿Componentes de una URL? 

Un URL se compone de los siguientes elementos: 

<br>

- Esquema/Protocolo: Indica el protocolo a usar (e.g., http://, https://). <br>

- Dominio/Host: El nombre del servidor o IP (e.g., www.ejemplo.com). <br>

- Puerto (opcional): Especifica el puerto (e.g., :8080). <br>

- Ruta/Path: La ubicación del recurso en el servidor (e.g., /articulos/). <br>

- Consulta/Query (opcional): Parámetros adicionales (e.g., ?id=123). <br>

- Fragmento (opcional): Un ancla dentro de la página (e.g., #seccion). <br>

 
<br><br>
 

### ¿Pasos en la recuperación de una página web mediante HTTP? 

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

### Diferencia entre páginas dinámicas y estáticas 

<br>

Páginas estáticas: 

 

- El contenido no cambia a menos que se edite manualmente el archivo. 

 

- Están predefinidas en archivos HTML que el servidor entrega tal cual al navegador. 

 

- Ejemplo: un sitio web de una empresa con información fija 

 <br>

Páginas dinámicas: 

 
- El contenido se genera en tiempo real, basado en solicitudes del usuario o datos del servidor. 

 

- Utilizan lenguajes de programación como PHP, Python o JavaScript para generar el HTML dinámicamente. 


- Ejemplo: una red social donde el contenido cambia según el usuario que accede. 

<br><br>
 
### ¿Cómo usar telnet para acceder a un servidor web? 

(solución en actividad 0.3) 

<br>
 
Request. Métodos principales 

Métodos: GET (envía recursos) y POST (envía datos para que sean procesados), PUT, HEAD y DELETE. 

<br> 

Response. Códigos:  

 
- Códigos con formato 1xx: Respuestas informativas. Indica que la petición ha sido recibida y se está procesando. 

- Códigos con formato 2xx: Respuestas correctas. Indica que la petición ha sido procesada correctamente. 

- Códigos con formato 3xx: Respuestas de redirección. Indica que el cliente necesita realizar más acciones para finalizar la petición. 

- Códigos con formato 4xx: Errores causados por el cliente. Indica que ha habido un error en el procesado de la petición a causa de que el cliente ha hecho algo mal. 

- Códigos con formato 5xx: Errores causados por el servidor. Indica que ha habido un error en el procesado de la petición a causa de un fallo en el servidor. 

 <br>

Content type. Tipos principales:  

- text: Indica que el contenido es texto plano. Ejemplos de subtipos: html, xml 

 

- multipart: Indica que tiene múltiples partes de datos independientes. Ejemplos de subtipos: form-data, digest 

 

- message: Para encapsular un mensaje existente. Por ejemplo cuando queremos responder a un mensaje de correo incorporando el mensaje origen. Ejemplos de subtipos: partial, rfc822 

 

- image: Indica que es una imagen. Ej de subtipos: png, gif 

 

- audio: Indica que es un audio. Ejemplos de subtipos: mp3, 32kadpcm 

 

- video: Indica que es un video. Ejemplos de subtipos: mpeg, avi 

 

- application: Indica que se trata de datos de aplicación los cuales pueden ser binarios. Ejemplos de subtipos: json, pdf 

<br><br>
 
## Actividad 0.2 - UDP and TCP: Comparison of Transport Protocols

[Video de referencia](https://www.youtube.com/watch?v=Vdc8TCESIg8)

### Diferencias entre UDP y TCP (min 2:46 y 4:15)

### Conexión

- **TCP**: Es un protocolo orientado a la conexión. Establece una conexión antes de enviar datos.
- **UDP**: Es un protocolo sin conexión. Envía datos sin establecer una conexión previa.

### Fiabilidad

- **TCP**: Garantiza la entrega de paquetes y el orden correcto. Realiza corrección de errores.
- **UDP**: No garantiza la entrega ni el orden. Es más rápido, pero menos fiable.

### Aplicaciones que utilizan TCP

- HTTP
- IMAP
- POP
- SMTP

### Aplicaciones que utilizan UDP

- DNS
- SNMP

### ¿Qué capa almacena el puerto?

**Capa de Transporte**: TCP y UDP utilizan números de puerto para identificar aplicaciones específicas.

### ¿Qué capa almacena la dirección IP?

**Capa de Red**: La dirección IP se utiliza para identificar dispositivos en una red.

<br><br>
¿Qué es three-way handshake? 

El three-way handshake (apretón de manos en tres pasos) es el proceso que utiliza el protocolo TCP para establecer una conexión confiable entre un cliente y un servidor antes de comenzar a intercambiar datos. Este mecanismo garantiza que ambas partes estén listas para la comunicación. 

 
### Actividad 0.3 - Práctica telnet/http 

https://www.youtube.com/watch?v=xpBpGC08f4Q&t=189s 

http://www.profesordeinformatica.com/servicios/http/telnet 

Lee el artículo y prueba los ejemplos sugeridos en él. 

Nota: Si usamos Windows 10, tenemos que activar “telnet” 

http://www.lawebdelprogramador.com/foros/Windows-10/1510815-Como-activar-Telnet-en-Windows-10.html 

<br>
 
Uso de comando telnet www.google.com 80 y luego GET / HTTP/1.1 para obtener el código de la página web: 

![image](https://github.com/user-attachments/assets/d74a0b84-931a-49ea-9330-5b1787a2f977)

<br>

Obtención de la página www.profesorinformatica.com:

![image](https://github.com/user-attachments/assets/a8c96eff-7efe-4e06-94c7-246e650da207)

<br><br>

## Actividad 0.4 - Usando curl 

https://curl.se/docs/manual.html

<br>

### Busca información sobre el comando curl y muestra al menos cinco ejemplos de uso:

a) Conseguir la página principal de un servidor web: 

![image](https://github.com/user-attachments/assets/9233fc06-f5fe-4cc0-b52e-5f5277748e2c)

b) Obtener archivo README de un servidor FTP: 

![image](https://github.com/user-attachments/assets/165afaf2-8c3d-4714-904a-d286895d5bff)

c) Listar directorios de servidor FTP: 

![image](https://github.com/user-attachments/assets/fc72a0e6-6f9e-41c7-87c1-4b93cd843169)

d) Obtener dos documentos a la vez: 

![image](https://github.com/user-attachments/assets/ab1cbbad-8cd2-40a4-a7c3-e9ad5bc6f548)

e) Descargar archivo de servidor FTPS: 

![image](https://github.com/user-attachments/assets/f918c793-6557-4092-a809-c15947afcf5c)


<br><br>

## Actividad 0.5 - Práctica servidor web 

<br>

1. Visita los siguientes enlaces:
   
Simple web server (ejemplo 1) 
https://docs.python.org/3/library/http.server.html
<br>
python -m http.server 8000 
<br>
http server (ejemplo 2) 
https://github.com/python/cpython/blob/main/Lib/http/server.py 
<br>
dummy web server (ejemplo 3) 
https://gist.github.com/kabinpokhrel/6fd1275603e9d5f1e284be717cbd1bff 
<br><br>
2. Instala Python.
<br><br>
3. Ejecuta los ejemplos mostrados con anterioridad.
<br><br>   
4. Publica en GitHub los ejemplos llevados a cabo. Los ejemplos se acompañarán con 
capturas de pantalla en las que se muestre su funcionamiento.
<br><br>

Ejemplo 1: 
Inicializamos el servidor web en el puerto 8000 y luego accedemos a localhost:8000 desde 
el navegador: 

<br>

![image](https://github.com/user-attachments/assets/be9581df-09d6-4d41-89e1-e3a8a301a451)

 
Ejemplo 3: 
 
Utilizamos el código de github y lo guardamos en la carpeta de usuario del equipo: 

![image](https://github.com/user-attachments/assets/d2473d7e-398f-4923-ad41-1003c2eef55f)

 
Ahora ejecutamos el comando python server.py:8000

![image](https://github.com/user-attachments/assets/43503b58-9fbc-4e86-9386-bdfc26eb16b7)

<br><br>

## Actividad 0.5. Repositorio Github 
<br>

Crea una cuenta en Github, si no la tienes ya. Crea un repositorio en Github con el nombre 
del módulo. El repositorio incluirá una carpeta para cada tema: “Tema0”, “Tema1”,... 
“TemaN” en el que incluirás las actividades que se te indiquen expresamente. 
El repositorio incluirá un archivo “README” en el que se enlazaran la solución a los 
ejercicios incluidos en las carpetas anteriores. 
La página README del repositorio debe tener un aspecto parecido al mostrado a 
continuación: 

![image](https://github.com/user-attachments/assets/84ccfc63-d93a-4b90-8413-55d9dc1dcc9a)


Nombre del módulo 
Este repositorio incluye actividades llevadas a cabo en el módulo 
nombredelmódulo 

Nota: Si no has utilizado antes Github, es recomendable que cree un repositorio nuevo 
llamado “prueba” que incluya una página “README.md”. Utiliza markdown para que incluya 
varias cabeceras, texto, una lista, un gráfico y una tabla. Previamente se recomienda leer: 
<br>
a. https://github.com/Github-Classroom-Cybros/Learn-Github 
b. https://guides.github.com/features/mastering-markdown/

![image](https://github.com/user-attachments/assets/b8e003f0-7e66-4179-9014-9fa1d91c3de8)

<br>

![image](https://github.com/user-attachments/assets/ca37e33a-c517-41c9-be01-ae5a470ee1e4)





