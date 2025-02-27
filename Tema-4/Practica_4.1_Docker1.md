
<p align="center">
  <img src="https://github.com/user-attachments/assets/92b13dd5-01d7-4f83-8bb6-e218dfb11235" alt="Descripción de la imagen"/>
</p>

# Práctica 4.1 - Tareas básicas con contenedores docker

## Ejercicios

<br>

### 1. **Ejecutar el contenedor hello-world**

```
docker run hello-world
```

<br>

![image](https://github.com/user-attachments/assets/fc9010e5-975b-44d4-93eb-21940f315ef7)

<br>

### 2. **Ver las imágenes de docker instaladas**

```
docker images
```

<br>

![image](https://github.com/user-attachments/assets/c0adb22d-90a6-4841-903c-63e532d43dc0)

<br>

### 3. **Mostrar los contenedores docker**

```
docker ps -a
```

<br>

![image](https://github.com/user-attachments/assets/b6f10dc0-b1c6-4e54-abbe-938391f90e4f)

<br>

### 4. **Crear un contenedor a través de un fichero dockerfile**

Nos clonamos el repositorio getting-started-app de docker:

```
git clone https://github.com/docker/getting-started-app.git
```

![image](https://github.com/user-attachments/assets/6f5d49fd-648e-4293-bc04-b382ac9e2714)

<br>

Creamos el fichero dockerfile y lo editamos:

```
nano dockerfile
```

![image](https://github.com/user-attachments/assets/599bc35c-83ab-4a12-a9ec-a1b3e9adf1d4)

![image](https://github.com/user-attachments/assets/4cbdd2fa-e3d3-418d-91ee-9b713807424b)

<br>

Construimos el contenedor:

```
 docker build -t getting-started .
```

<br>

![image](https://github.com/user-attachments/assets/da47399e-7700-416f-b77d-38c61d548b63)

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




















 

  
 

