<p align="center">
  <img src="https://github.com/user-attachments/assets/92b13dd5-01d7-4f83-8bb6-e218dfb11235" alt="Descripción de la imagen"/>
</p>

# 🖥️ Práctica Autenticación y SSL

---

## 🎯 Objetivo
Configurar la autenticación y encriptación de una página apache

---

## Autenticación

### 1. Intalación del servidor LAMP:

```apt-get install apache2 php7.0 libaprutil1-dbd-mysql -y```

![image](https://github.com/user-attachments/assets/20aa1cf6-00a2-4063-a425-462cb8c2624c)


### 2. Instalación de MYSQL:

```apt-get update -y```
```apt-get install mariadb-server mariadb-client -y```

![image](https://github.com/user-attachments/assets/3e486a09-cb01-470b-90d0-cfc01e8066a6)


### 3. Activación de los servicios:

```systemctl start apache2```
```systemctl start mysql```
```systemctl enable apache2```
```systemctl enable mysql```

![image](https://github.com/user-attachments/assets/4fb7d718-66ee-45c5-9e46-bb41d72e7543)

### 4. Configuración de la base de datos:

Iniciar como root:

```mysql -u root -p```

![image](https://github.com/user-attachments/assets/16137335-f010-4bde-bdec-d4eff993e09c)

Crear la base de datos:

```create database defaultsite_db; ```

![image](https://github.com/user-attachments/assets/86a82f60-9411-4da6-afb3-6204f6495ff1)

Damos privilegios a sobre la base de datos al usuario administrador:

```GRANT SELECT, INSERT, UPDATE, DELETE ON defaultsite_db.* TO 'defaultsite_admin'@'localhost' IDENTIFIED BY 'password';```

```GRANT SELECT, INSERT, UPDATE, DELETE ON defaultsite_db.* TO 'defaultsite_admin'@'localhost.localdomain' IDENTIFIED BY 'password';```

![image](https://github.com/user-attachments/assets/63baeda9-4210-4eb8-90bf-806bb3210b45)

![image](https://github.com/user-attachments/assets/203b6e56-dfb9-4449-9b82-b30c65a45ec0)

Actualizamos los privilegios:

```flush privileges;```

![image](https://github.com/user-attachments/assets/1299c732-4b9d-4e61-bdff-7016bcafb54a)

Creamos la tabla que almacenará los datos de autenticación:

```use defaultsite_db;```

![image](https://github.com/user-attachments/assets/345daab3-0151-4720-8f4a-67585b17660a)

Introducimos los datos del usuario con la contraseña encriptada:

```htpasswd -bns siteuser siteuser```

```create table mysql_auth ( username varchar(191) not null, passwd varchar(191), groups varchar(191), primary key (username) );```

```INSERT INTO `mysql_auth` (`username`, `passwd`, `groups`) VALUES('siteuser', '{SHA}tk7HEH6Wo7SKT6+3FHCgiGnJ6dA=', 'sitegroup'); ```

![image](https://github.com/user-attachments/assets/7800439a-50d5-4aad-a57f-9d579db61947)

![image](https://github.com/user-attachments/assets/6267c553-747d-46c3-9542-61042629b733)

![image](https://github.com/user-attachments/assets/4e8d2cdd-b447-4f47-b246-05c395f4d09f)

### 5. Configuración de apache

Activamos los módulos necesarios:

```a2enmod dbd ```
```a2enmod authn_dbd ```
```a2enmod socache_shmcb ```
```a2enmod authn_socache ```

![image](https://github.com/user-attachments/assets/2a18cf9c-23f3-4a54-9041-9269b26d554f)

Creamos el recurso protegido en /var/www/html:

```mkdir /var/www/html/protecteddir```
```chown -R www-data:www-data /var/www/html/protecteddir```

![image](https://github.com/user-attachments/assets/dd9a9208-473e-4f94-b82f-8879528a7d5d)

Modificamos el archivo de configuración por defecto de sites-available:

```nano /etc/apache2/sites-available/000-default.conf```

![image](https://github.com/user-attachments/assets/9155fc11-aff9-4dbe-ab9d-e1254afe510b)

Reiniciamos apache y comprobamos el funcionamiento:

![image](https://github.com/user-attachments/assets/2f5919c0-adaf-4c30-aec7-4cffb5c92fa2)

![image](https://github.com/user-attachments/assets/962095dc-5734-4487-8305-6ff368604d92)

![image](https://github.com/user-attachments/assets/c79e2bb7-a85d-4b52-b037-145ec8be733f)

<br>

## SSL

1. Activar el módulo ssl:

```a2enmod ssl ```

```systemctl restart apache2 ```

![image](https://github.com/user-attachments/assets/7535855f-4e69-4956-82f6-6d9387042c50)

2. Crear el certificado ssl:

![image](https://github.com/user-attachments/assets/ff28122e-d4cc-4933-8fd5-644ea7f0e9d1)

3. Configurar apache para usar ssl:

```sudo nano /etc/apache2/sites-available/default-ssl.conf```

![image](https://github.com/user-attachments/assets/752f1056-c9b5-4e4b-a866-3d9df1d3fb16)

4. Activamos la configuración y comprobamos el funcionamiento: (Para confiar en la página hay que instalar el certificado)

```a2ensite default-ssl.conf```

![{67412A6E-4A2E-42E7-A34A-AFFB4EC60F68}](https://github.com/user-attachments/assets/b613f902-4cd5-43b6-89a5-792a2d23f02c)

![{A105B561-C647-4B07-87E3-65DF75F971D5}](https://github.com/user-attachments/assets/3de58add-17f4-487c-a061-dffb921c305c)

![{FFF26439-8747-4340-85B0-E1D9CCC08307}](https://github.com/user-attachments/assets/bc19a044-02c7-4f7a-b4d5-ae5c8bf3efa1)










































