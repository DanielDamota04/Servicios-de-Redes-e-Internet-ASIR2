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

2. **Activación de módulos para PHP y MySQL**:
   - Activar los módulos necesarios para ejecutar PHP y permitir el acceso a bases de datos en MySQL.
  
     <br>

3. **Instalación y Configuración de WordPress**.
   - Configura WordPress en `centro.intranet`.
  
     <br>

4. **Activación del módulo WSGI**:
   - Habilitar el módulo `wsgi` en Apache para permitir la ejecución de aplicaciones en Python.
  
     <br>

5. **Despliegue de una Aplicación Python**.
   - Crea y despliega una pequeña aplicación en Python en `departamentos.centro.intranet` para verificar su correcto funcionamiento.
   - Añadir autenticación para proteger el acceso a la aplicación Python.
  
     <br>

6. **Instalación y configuración de Awstat**.
   - Configura Awstat para analizar el tráfico del servidor.
  
     <br>

7. **Configuración de un segundo servidor web**:
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

