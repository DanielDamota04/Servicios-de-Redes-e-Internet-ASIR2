<p align="center">
  <img src="https://github.com/user-attachments/assets/92b13dd5-01d7-4f83-8bb6-e218dfb11235" alt="Descripción de la imagen"/>
</p>

<br>

# Práctica Servidores Web (Primer Trimestre)

<br>

## Objetivo
Instalar y configurar un servidor web interno para un instituto.

<br>

### Requisitos

<br>

1. **Instalación del servidor web Apache**.
   - Configurar dos dominios mediante el archivo `/etc/hosts`: 
     - `centro.intranet` (para servir contenido mediante WordPress).
     - `departamentos.centro.intranet` (para una aplicación en Python).
    
  Instalar servidor web apache:
    
  ![{C98F05DA-5E0C-47B5-B361-18529197312C}](https://github.com/user-attachments/assets/6e808256-128c-4063-862f-c6e2cde95d11)

  <br>
  
  Comprobación de la instalación:

  ![image](https://github.com/user-attachments/assets/78f303da-731e-48b5-9fd7-73897c6f61f2)


  <br>

2. **Activación de módulos para PHP y MySQL**:
   - Activar los módulos necesarios para ejecutar PHP y permitir el acceso a bases de datos en MySQL.
  
     <br>

     Instalación de MySQL:

     ![image](https://github.com/user-attachments/assets/23168866-2ca2-4aeb-8baf-5e1e4572dcb0)

     <br>

     Comprobación de la instalación:

     ![image](https://github.com/user-attachments/assets/16f819a0-e68f-43e8-8d74-946d47ea0691)

     <br>

     Instalación de PHP:

     ![image](https://github.com/user-attachments/assets/58edefc6-dc9b-4f32-9a15-c4161ce07543)

     <br>

     Comprobación de la instalación:

     ![image](https://github.com/user-attachments/assets/fc4e8d29-d00b-46dd-ba60-3ab2748fe3e2)

     Modificación del fichero hosts:

     ![image](https://github.com/user-attachments/assets/1f514793-a9b2-4a89-bc04-f94af106b3ba)


4. **Instalación y Configuración de WordPress**.
   - Configura WordPress en `centro.intranet`.
  
     <br>

     Instalación de wordpress:

     ![image](https://github.com/user-attachments/assets/101b319b-fc6b-4ff9-b908-0f55e3aec328)

     Descomprimimos la carpeta:

     ![image](https://github.com/user-attachments/assets/fcd30977-511b-40fa-b09c-97b6d88e1559)

     Movemos el contenido de la carpeta a /var/www/centro.intranet:

     ![image](https://github.com/user-attachments/assets/051c4fc7-9d44-4f9a-baff-3448c1680cf8)

     Eliminamos la carpeta de wordpress:

     ![image](https://github.com/user-attachments/assets/a63c4f7a-4893-4eb4-ad17-6713cc125de2)

     Configuramos el virtualhost:

     ![image](https://github.com/user-attachments/assets/b04b91e9-3c95-4e79-bac6-f775913d70bd)

     Habilitamos el virtualhost:

     ![image](https://github.com/user-attachments/assets/d71b8e20-a4e5-48af-ac58-227615f6657a)
  
     Reiniciamos Apache:
  
     ![image](https://github.com/user-attachments/assets/3109d2fa-aa77-4e12-aaf0-99d1e507514f)

     Accedemos a centro.intranet:

     ![image](https://github.com/user-attachments/assets/5e4573f1-04e9-49cb-8abc-6e41ce94825d)


6. **Activación del módulo WSGI**:
   - Habilitar el módulo `wsgi` en Apache para permitir la ejecución de aplicaciones en Python.
  
     <br>

7. **Despliegue de una Aplicación Python**.
   - Crea y despliega una pequeña aplicación en Python en `departamentos.centro.intranet` para verificar su correcto funcionamiento.
   - Añadir autenticación para proteger el acceso a la aplicación Python.
  
     <br>

8. **Instalación y configuración de Awstat**.
   - Configura Awstat para analizar el tráfico del servidor.
  
     <br>

9. **Configuración de un segundo servidor web**:
   - Instalar y configurar un segundo servidor (Nginx o Lighttpd) bajo el dominio `servidor2.centro.intranet`.
   - Configurarlo para servir en el puerto `8080`.
   - Habilitar PHP en el servidor y añadir `phpMyAdmin`.

---

### Exposición Final
Al finalizar el trabajo, se realizará una exposición con una presentación de los resultados.

---

### Enlaces de Interés
- [Python bajo Apache](https://uniwebsidad.com/libros/python/capitulo-13/python-bajo-apache)

---

### Instrucciones de Entrega

1. Crear un repositorio en **GitHub** para documentar los pasos realizados en cada una de las actividades.
   - La documentación debe incluir:
     - Fragmentos de código usados.
     - Imágenes que muestren las pantallas del proceso en la máquina virtual.
2. El enlace al repositorio de GitHub debe agregarse al repositorio del módulo, especificando claramente que corresponde a la práctica de servidores web.

---

### Fecha de Entrega
La fecha límite de entrega es el **5 de diciembre**.

