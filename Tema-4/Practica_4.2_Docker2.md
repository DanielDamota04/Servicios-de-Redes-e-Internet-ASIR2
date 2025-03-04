
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

### 6. **Ejecutar un contenedor hello-world y darle nombre “myhello2”**

```
docker run --name myhello2 hello-world
```

![image](https://github.com/user-attachments/assets/3e500a4d-e1b9-4eeb-ab07-0dd30ec6203d)

![image](https://github.com/user-attachments/assets/f4e48e18-267c-412a-891b-35a68c291ec6)

<br>

### 7. **Ejecutar un contenedor hello-world y darle nombre “myhello3**

```
docker run --name myhello3 hello-world
```
<br>

![image](https://github.com/user-attachments/assets/d2502415-72dd-4785-98b7-bfe757b42ae8)

![image](https://github.com/user-attachments/assets/e279308b-ab11-4d6e-af41-55119bdd21e0)


<br>

### 8. **Mostrar los contenedores que se están ejecutando**

![image](https://github.com/user-attachments/assets/8db07428-3a5f-4346-95e4-f2bedbce2c8e)

<br>

### 9. **Para el contenedor "myhello1"**

```
docker stop myhello1
```

<br>

### 10. **Para el contenedor "myhello2"**

```
docker stop myhello2
```
<br>

### 11. ** Borra el contenedor "myhello1"**

```
docker rm myhello1
```

![image](https://github.com/user-attachments/assets/416e025f-5365-4a68-ae6f-2a14d6ba849d)


<br>

### 12. **Borra todos los contenedores detenidos**

```
docker container prune -f
```

![image](https://github.com/user-attachments/assets/e7f04b62-0f6e-4a40-8ae8-0d19f7a818b2)



















 

  
 
