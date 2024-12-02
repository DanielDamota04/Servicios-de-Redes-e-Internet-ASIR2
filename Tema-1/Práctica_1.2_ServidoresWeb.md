<p>
  <img src="https://github.com/user-attachments/assets/92b13dd5-01d7-4f83-8bb6-e218dfb11235" alt="Descripción de la imagen"/>
</p>

# 🖥️ Práctica Servidores Web (Primer Trimestre)

---

## 🎯 Objetivo
Instalar y configurar un servidor web interno para un instituto.

---

## 📋 Requisitos

### 1. Instalación del servidor web Apache
- Configurar dos dominios mediante el archivo `/etc/hosts`: 
  - `centro.intranet` (para servir contenido mediante WordPress).
  - `departamentos.centro.intranet` (para una aplicación en Python).

#### Instalación del servidor web Apache:
![Instalación de Apache](https://github.com/user-attachments/assets/6e808256-128c-4063-862f-c6e2cde95d11)

#### Comprobación de la instalación:
![Comprobación de Apache](https://github.com/user-attachments/assets/78f303da-731e-48b5-9fd7-73897c6f61f2)

---

### 2. Activación de módulos para PHP y MySQL
Activar los módulos necesarios para ejecutar PHP y permitir el acceso a bases de datos en MySQL.

#### Instalación de MySQL:
![Instalación de MySQL](https://github.com/user-attachments/assets/23168866-2ca2-4aeb-8baf-5e1e4572dcb0)

#### Comprobación de la instalación:
![Comprobación de MySQL](https://github.com/user-attachments/assets/16f819a0-e68f-43e8-8d74-946d47ea0691)

#### Instalación de PHP:
![Instalación de PHP](https://github.com/user-attachments/assets/58edefc6-dc9b-4f32-9a15-c4161ce07543)

#### Comprobación de la instalación:
![Comprobación de PHP](https://github.com/user-attachments/assets/fc4e8d29-d00b-46dd-ba60-3ab2748fe3e2)

#### Modificación del fichero hosts:
![Modificación del hosts](https://github.com/user-attachments/assets/1f514793-a9b2-4a89-bc04-f94af106b3ba)

---

### 3. Instalación y Configuración de WordPress
Configura WordPress en `centro.intranet`.

#### Instalación de WordPress:
![Instalación de WordPress](https://github.com/user-attachments/assets/101b319b-fc6b-4ff9-b908-0f55e3aec328)

#### Descomprimimos la carpeta:
![Descomprimir WordPress](https://github.com/user-attachments/assets/fcd30977-511b-40fa-b09c-97b6d88e1559)

#### Movemos el contenido de la carpeta a `/var/www/centro.intranet`:
![Mover contenido](https://github.com/user-attachments/assets/051c4fc7-9d44-4f9a-baff-3448c1680cf8)

#### Eliminamos la carpeta de WordPress:
![Eliminar carpeta WordPress](https://github.com/user-attachments/assets/a63c4f7a-4893-4eb4-ad17-6713cc125de2)

#### Configuramos el virtualhost:
![Configuración del VirtualHost](https://github.com/user-attachments/assets/b04b91e9-3c95-4e79-bac6-f775913d70bd)

#### Habilitamos el virtualhost:
![Habilitar VirtualHost](https://github.com/user-attachments/assets/d71b8e20-a4e5-48af-ac58-227615f6657a)

#### Reiniciamos Apache:
![Reiniciar Apache](https://github.com/user-attachments/assets/3109d2fa-aa77-4e12-aaf0-99d1e507514f)

#### Accedemos a `centro.intranet`:
![Acceso a centro.intranet](https://github.com/user-attachments/assets/5e4573f1-04e9-49cb-8abc-6e41ce94825d)

#### Creamos la base de datos para WordPress:
![Crear base de datos](https://github.com/user-attachments/assets/3f08e812-8486-4084-a9a4-7a6fe021658b)

#### Creamos el usuario administrador para la base de datos de WordPress:
![Crear usuario administrador](https://github.com/user-attachments/assets/857fe25b-bfb1-4dd6-9805-ec786b174af4)

#### Para otorgarle al usuario permisos, hay que iniciar como root:
![Iniciar como root](https://github.com/user-attachments/assets/596aab5d-9534-4928-9beb-de9192848723)

#### Le otorgamos permisos al usuario admin:
![Otorgar permisos](https://github.com/user-attachments/assets/f49db8bd-3ec4-4a7d-b86c-a7d5c43ef78e)

#### Ya podemos instalar WordPress:
![Instalación de WordPress completada](https://github.com/user-attachments/assets/40323c20-7c25-410b-afe4-80a6696a90a6)

#### En el siguiente paso te pide que copies un contenido al archivo wp-config.php, en los archivos de wordpress hay uno llamado wp-config-sample.php, suyo objetivo es ser la plantilla del archivo wp-config.php:
![Crear wp-config.php](https://github.com/user-attachments/assets/199285e2-7710-40bf-a7bf-a918fe1e146c)

#### Modificamos el contenido del archivo `wp-config.php`:
![Modificar wp-config.php](https://github.com/user-attachments/assets/d5a9baf6-092e-45d8-ab80-16055005ef8b)

#### Ahora ya podemos continuar con la instalación:
![Continuar instalación](https://github.com/user-attachments/assets/e6fde765-a6c7-4b92-b650-194d0c5e7f1e)

#### Ya hemos instalado WordPress:
![WordPress instalado](https://github.com/user-attachments/assets/73b1b86d-169f-405e-b797-d0cef14af406)

#### Accedemos al dashboard:
![Acceso al dashboard](https://github.com/user-attachments/assets/88f84749-623e-4623-ba65-ec598a51bc6d)

---

### 4. Activación del módulo WSGI
Habilitar el módulo `wsgi` en Apache para permitir la ejecución de aplicaciones en Python.

Creamos el directorio para departamentos.centro.intranet en /var/www y habilitamos el módulo wsgi:

![image](https://github.com/user-attachments/assets/66762bde-aa45-4b8d-9c08-06bb7962f3c0)

Comprobamos que el módulo wsgi está activado:

![image](https://github.com/user-attachments/assets/1656a168-199a-461f-adbf-f0786796b948)

Configuramos el virtualhost:

![image](https://github.com/user-attachments/assets/ddc7a29b-043a-4011-b25f-c0a7d7ea734b)

Habilitamos el virtualhost:

![image](https://github.com/user-attachments/assets/c622336a-de6b-4219-a43a-6e2187f63ea2)

Creamos el archivo python:

![image](https://github.com/user-attachments/assets/2212ac30-a4d0-48ea-9f4f-7b8948a1c61f)

Reiniciamos apache:

![image](https://github.com/user-attachments/assets/2f95ec0a-01ad-422c-96c7-1d7782f4a820)

---

### 5. Despliegue de una Aplicación Python
- Crea y despliega una pequeña aplicación en Python en `departamentos.centro.intranet` para verificar su correcto funcionamiento.
- Añadir autenticación para proteger el acceso a la aplicación Python.

Accedemos a departamentos.centro.intranet para verificar el funcionamiento del archivo python creado en el apartado anterior:

![image](https://github.com/user-attachments/assets/a73e620f-9ed7-4a04-b76e-17d715cc7879)

Autenticación para proteger el acceso a la aplicación (uso de contraseñas):

Para empezar creamos un archivo para  guardar los usuarios y contraseñas en un lugar no accesible fuera del equipo:

![image](https://github.com/user-attachments/assets/e49cb8e7-aa79-43f4-8e61-c7d480c46bc4)

Creamos los usuarios y contraseñas los cuales se autenticarán:

![image](https://github.com/user-attachments/assets/76ac95fa-7138-44cd-a912-f2bd8e01f932)

Configuramos el virtualhost de departamentos.centro.intranet:

![image](https://github.com/user-attachments/assets/9a4831de-163f-4160-85bb-26fbacdc9a39)

Intentamos acceder a departamentos.centro.intranet y nos pedirá el usuario:

![image](https://github.com/user-attachments/assets/ed654dac-6ba4-4202-b653-81ed2121a6b8)

Introducimos las credenciales y podemos acceder

![image](https://github.com/user-attachments/assets/cd6066bd-a856-4960-a5c1-27cabb100646)

---

### 6. Instalación y configuración de Awstat
Configura Awstat para analizar el tráfico del servidor.

Instalamos awstats:

![image](https://github.com/user-attachments/assets/8a53b70f-4210-4102-bd4c-7afe5eeeb15c)

Activamos el módulo cgi:

![image](https://github.com/user-attachments/assets/3ba4977a-acc2-4543-a3e6-5793134fd89f)

Reiniciamos apache:

![image](https://github.com/user-attachments/assets/b343c86e-6bbd-4e38-9099-1047e7e042da)

Ahora configuramos awstats para el dominio de centro.intranet:

![image](https://github.com/user-attachments/assets/72cdca78-cf7c-42d8-a811-323071218b3e)

Elegimos el dominio y el host:

![image](https://github.com/user-attachments/assets/b707d3fe-8577-4dca-bc32-a01f67c42e10)

Activamos que se actualicen las estadísticas:

![image](https://github.com/user-attachments/assets/3c65a7e9-ca70-4a5d-86c8-ed8114747401)

Generamos las primeras estadísticas:

![image](https://github.com/user-attachments/assets/946b3ea6-f9f9-4522-9736-df501b909318)

Realizamos la configuración para apache y asignamos permisos:

![image](https://github.com/user-attachments/assets/f4cbf009-65bf-4630-946d-335d2f118394)

![image](https://github.com/user-attachments/assets/513e2d23-cf5b-408e-9380-d201407aaa16)

![image](https://github.com/user-attachments/assets/d96e3492-b9ae-4658-b53b-825d5c3c17bf)

Modificamos la configuración de awstats dentro de apache:

![image](https://github.com/user-attachments/assets/63f2d2de-c109-4386-94cb-850b5d70a36c)

Agregamos lo siguiente:

![image](https://github.com/user-attachments/assets/da818292-bdb5-4425-9140-53e3f6379820)

Habilitamos la configuración y reiniciamos apache:

![image](https://github.com/user-attachments/assets/e02783c4-6a28-436c-89ce-f623cfc2f76c)

![image](https://github.com/user-attachments/assets/3dc72067-cace-49e0-9b23-5066dd1b0bba)















---

### 7. Configuración de un segundo servidor web
- Instalar y configurar un segundo servidor (Nginx o Lighttpd) bajo el dominio `servidor2.centro.intranet`.
- Configurarlo para servir en el puerto `8080`.
- Habilitar PHP en el servidor y añadir phpMyAdmin.

---

### 🎤 Exposición Final
Al finalizar el trabajo, se realizará una exposición con una presentación de los resultados.

---

### 🔗 Enlaces de Interés
- [Python bajo Apache](https://uniwebsidad.com/libros/python/capitulo-13/python-bajo-apache)

---

### 📅 Instrucciones de Entrega
1. Crear un repositorio en **GitHub** para documentar los pasos realizados en cada una de las actividades.
   - La documentación debe incluir:
     - Fragmentos de código usados.
     - Imágenes que muestren las pantallas del proceso en la máquina virtual.
2. El enlace al repositorio de GitHub debe agregarse al repositorio del módulo, especificando claramente que corresponde a la práctica de servidores web.

---

### 📅 Fecha de Entrega
La fecha límite de entrega es el **5 de diciembre**.
