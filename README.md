# Parcial Diseño y Arquitectura de software

Pasos para iniciar la aplicación:

* Crear una network para la conexión entre el contenedor de mysql:
  docker network create red
* Crear un contenedor de mysql y asignar la red:
  docker run --name BD -e MYSQL_PASSWORD=clave -e MYSQL_USER=root -e MYSQL_DATABASE=yms -d -p 8085:3306 mysql
* Crear una imagen de la aplicación, dentro del archivo del app:
 docker build -t app:1.0.0
* Crear un contenedor de la aplicación:
 docker run -d -p 8080:8080 -n red app:1.0.0 
 
  
