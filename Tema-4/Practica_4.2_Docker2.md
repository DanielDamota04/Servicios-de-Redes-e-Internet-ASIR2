
<p align="center">
  <img src="https://github.com/user-attachments/assets/92b13dd5-01d7-4f83-8bb6-e218dfb11235" alt="Descripción de la imagen"/>
</p>

# Práctica 4.2 - Tareas básicas con contenedores docker (Parte 2)

## Ejercicios

<br>

### 1. **Descarga la imagen de ubuntu**

```
docker pull ubuntu
```

<br>

![image](https://github.com/user-attachments/assets/430fb910-7645-41fe-bd96-6e6f50cab734)


<br>

### 2. **Descarga la imagen de hello-world**

```
docker pull hello-world
```

<br>

![image](https://github.com/user-attachments/assets/691762d0-9be6-4583-af39-9bb1846124ba)

<br>

### 3. **Descarga la imagen nginx**

```
docker pull nginx
```

<br>

![image](https://github.com/user-attachments/assets/890f7fe9-e062-4a27-b20d-5bb6f3356f04)

<br>

### 4. **Mostrar un listado de todas las imágenes**

```
docker images
```

![image](https://github.com/user-attachments/assets/572dd7a2-80e5-464d-9b9f-9ff99577db9b)


<br>

### 5. **Ejecutar un contenedor hello-world y darle nombre “myhello1”**

```
docker run --name myhello1 hello-world
```

![image](https://github.com/user-attachments/assets/8d6bf194-8af6-4873-a8c8-efb2e3960fd2)


![image](https://github.com/user-attachments/assets/bf939656-9709-45e4-902f-16e79f490afb)


<br>

### 6. **ejecutar un contenedor hello-world y darle nombre “myhello2”**

```
docker run --name myhello2 hello-world
```

![image](https://github.com/user-attachments/assets/3e500a4d-e1b9-4eeb-ab07-0dd30ec6203d)




<br>

Iniciamos el contenedor, haciendo tunneling para acceder desde localhost al servicio web:

```
docker build -t getting-started .
```
<br>

![image](https://github.com/user-attachments/assets/11b027ac-e25b-4cd1-80f4-7771003119d2)

![image](https://github.com/user-attachments/assets/a070a969-3fd1-41bc-88f8-4b38a7b7198e)

<br>

Creamos una cuenta de hub.docker.com:

![image](https://github.com/user-attachments/assets/e85e949c-fb37-495a-a0dd-2865220a95a5)

![image](https://github.com/user-attachments/assets/904892bf-9529-490b-8483-4ecdff622345)

<br>

Publicamos el contenedor:

1) Creamos el repositorio donde alojaremos el contenedor:

![image](https://github.com/user-attachments/assets/62b37ab1-3891-49ec-9e11-dda7cff6c6a5)

![image](https://github.com/user-attachments/assets/820817c4-3dd7-4cf0-8003-9c275a970d5a)

<br>

2) Iniciamos sesion en docker hub desde la terminal:

```
docker login -u YOUR-USER-NAME
```

![image](https://github.com/user-attachments/assets/1264eb2d-cb2d-419c-9bfe-0372714367c5)

3) Usamos docker tag para asignar un nuevo nombre a la imagen de getting-started:

```
docker tag getting-started YOUR-USER-NAME/getting-started
```

![image](https://github.com/user-attachments/assets/9c7330f5-0077-4f5d-ad9d-5cac2aaacfaf)

<br>

4) Publicamos el contenedor:

```
docker push YOUR-USER-NAME/getting-started
```




















 

  
 
