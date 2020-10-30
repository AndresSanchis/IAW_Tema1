# 1.- Instalación de DOCKER

Antes de la instalación haremos un "sudo apt-get update" y una vez actualizados los repositorios instalaremos Docker usando el "sudo apt-get install docker".

# 2.- Creación del contenedor de Nginx

Una vez instalado el Docker creamos un contenedor de Nginx usando el comando "docker pull nginx", con esto ya tenemos el contenedor pero ahora hay que arrancarlo. Para esto esamos "docker run -d -p 8888:80 nginx nginx_andres nginx" con esto canviamos el puerto de nuestro nginx al 8888.

# 3.- Nuestro sitio en nginx con Docker

Ahora añadimos nuestro sitio creado anterior mente en Hugo al nginx, para ello usamos "docker run -d -p 8888:80 --name nginx_andres -v /home/andres/andres/public/:/usr/share/nginx/html:ro nginx".
Una vez ejecutado este comando ya podremos acceder a nuestro sitio web desde el navegador usando la ip 127.0.0.1 y el puerto 8888.
