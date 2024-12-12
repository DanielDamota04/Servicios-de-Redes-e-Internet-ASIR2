<p align="center">
  <img src="https://github.com/user-attachments/assets/92b13dd5-01d7-4f83-8bb6-e218dfb11235" alt="Descripción de la imagen"/>
</p>

# 🖥️ Práctica Autenticación y SSL

---

## 🎯 Objetivo
Configurar la autenticación y encriptación de una página apache

---

### Autenticación

1. Intalación del servidor LAMP:

```apt-get install apache2 php7.0 libaprutil1-dbd-mysql -y```

2. Instalación de MYSQL:

```apt-get update -y```
```apt-get install mariadb-server mariadb-client -y```

3. Activación de los servicios:

```systemctl start apache2```
```systemctl start mysql```
```systemctl enable apache2```
```systemctl enable mysql```

4. Configuración de la base de datos:

Iniciar como root:

```mysql -u root -p```

Crear la base de datos:

```create database defaultsite_db; ```

Damos privilegios a sobre la base de datos al usuario administrador:

```GRANT SELECT, INSERT, UPDATE, DELETE ON defaultsite_db.* TO 'defaultsite_admin'@'localhost' IDENTIFIED BY 'password';```
```GRANT SELECT, INSERT, UPDATE, DELETE ON defaultsite_db.* TO 'defaultsite_admin'@'localhost.localdomain' IDENTIFIED BY 'password';```

Actualizamos los privilegios:

```flush privileges;```

Creamos la tabla que almacenará los datos de autenticación:

```use defaultsite_db;```

Introducimos los datos del usuario con la contraseña encriptada:

```htpasswd -bns siteuser siteuser```









