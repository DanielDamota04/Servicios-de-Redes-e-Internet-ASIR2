# 1. Despliegue de Wordpress + mariadb

Para la instalación de WordPress necesitamos dos contenedores: la base de datos (imagen `mariadb`) y el servidor web con la aplicación (imagen `wordpress`). Los dos contenedores tienen que estar en la misma red y deben tener acceso por nombres (resolución DNS) ya que de principio no sabemos que ip va a coger cada contenedor. Por lo tanto vamos a crear los contenedores en la misma red:

```bash
$ docker network create red_wp
```

![image](https://github.com/user-attachments/assets/1892aad2-d635-409f-b431-e3eafab6ab1f)


Siguiendo la documentación de la imagen [mariadb](https://hub.docker.com/_/mariadb) y la imagen [wordpress](https://hub.docker.com/_/wordpress) podemos ejecutar los siguientes comandos para crear los dos contenedores:

```bash
$ docker run -d --name servidor_mysql \
                --network red_wp \
                -v /opt/mysql_wp:/var/lib/mysql \
                -e MYSQL_DATABASE=bd_wp \
                -e MYSQL_USER=user_wp \
                -e MYSQL_PASSWORD=asdasd \
                -e MYSQL_ROOT_PASSWORD=asdasd \
                mariadb
                
$ docker run -d --name servidor_wp \
                --network red_wp \
                -v /opt/wordpress:/var/www/html/wp-content \
                -e WORDPRESS_DB_HOST=servidor_mysql \
                -e WORDPRESS_DB_USER=user_wp \
                -e WORDPRESS_DB_PASSWORD=asdasd \
                -e WORDPRESS_DB_NAME=bd_wp \
                -p 80:80 \
                wordpress

$ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                NAMES
5b2c5a82a524        wordpress           "docker-entrypoint.s…"   9 minutes ago       Up 9 minutes        0.0.0.0:80->80/tcp   servidor_wp
f70f22aed3d1        mariadb             "docker-entrypoint.s…"   9 minutes ago       Up 9 minutes        3306/tcp             servidor_mysql
```
---

![image](https://github.com/user-attachments/assets/82576e73-2ae6-4724-94de-65ecf0521a1f)

![image](https://github.com/user-attachments/assets/7008b3c0-e848-41e7-8d8d-27fa151a54a8)

![image](https://github.com/user-attachments/assets/994e4db9-23d2-45da-a87a-fd5632862c19)

Visualizamos la ip del contenedor para acceder via web:

```
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' servidor_wp
```

![image](https://github.com/user-attachments/assets/7b8f954b-e8b6-473f-a53f-cb1978ffa3e1)

Accedemos desde el navegador:

![image](https://github.com/user-attachments/assets/c0307c53-c263-4f66-a875-18d1d10088c0)

---

# 1. Despliegue de Tomcat + Nginx

En este ejemplo vamos a desplegar una aplicación muy sencilla en un servidor de aplicación Tomcat, a la que accederemos utilizando un proxy inverso nginx. En este ejercicio, además de seguir trabajando con las redes de tipo bridge definida por el usuario, vamos a usar bind mount para montar los ficheros de configuración y de despliegue en los contenedores.

## Desplegando tomcat

Antes de hacer el despliegue del primer contenedor, vamos a crear una red bridge para conectar los contenedores:

```
docker network create red_tomcat
```

![image](https://github.com/user-attachments/assets/63c66601-7bc2-46c3-b07e-cc1df29594b0)


A continuación vamos a crear un contenedor a partir de la imagen [`tomcat`](https://hub.docker.com/_/tomcat). En la documentación podemos ver que el directorio `/usr/local/tomcat/webapps/` es donde tenemos que poner el fichero de despliegue `war` (vamos a usar **bind mount** para montar el fichero war en el directorio). No vamos a mapear puerto porque no vamos a acceder a este contenedor desde el exterior.

![image](https://github.com/user-attachments/assets/b3b620ee-90c4-45e7-8c40-a7a83ddae446)


```bash
$ cd tomcat
~/tomcat$ ls
default.conf  sample.war
```

Y creamos el contenedor conectada a nuestra nueva red:

```bash
$ docker run -d --name aplicacionjava \
                --network red_tomcat \
                -v /home/vagrant/tomcat/sample.war:/usr/local/tomcat/webapps/sample.war:ro \
                tomcat:9.0
```

## Desplegando nginx como proxy inverso

Como vimos anteriormente en el directorio de trabajo tenemos también la configuración de nginx para que funcione como proxy inverso:

```bash
server {
    listen       80;
    listen  [::]:80;
    server_name  localhost;

    location / {
        root   /usr/share/nginx/html;
	proxy_pass http://aplicacionjava:8080/sample/;
    }
    error_page   500 502 503 504  /50x.html;
    location = /50x.html {
        root   /usr/share/nginx/html;
    }
}
```
Como vemos para realizar el proxy inverso usamos la directiva `proxy_pass`indicando la dirección que nos ofrece tomcat, en este caso usamos el nombre del contenedor anterior (`aplicacionjava`) que será resuelto por el servidor DNS interno, usando el puerto estándar de tomcat el 8080 y el directorio `sample` donde se ha desplegado la aplicación. Para la creación del contenedor de nginx:

```bash
$ docker run -d --name proxy \
                -p 80:80 \
                --network red_tomcat \
                -v /home/vagrant/tomcat/default.conf:/etc/nginx/conf.d/default.conf:ro \
                nginx
```

Y al acceder la ip de nuestro host:







