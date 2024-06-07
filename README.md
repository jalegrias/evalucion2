**Levantar Imagen NAGIOS**

> Se clona desde GitHub:
[Evalucion2](https://github.com/jalegrias/evalucion2.git)

- Se ejecuta el comando:
1. docker-compose up -d

version: '3'
services:
  nagios:
    image: "srbooz/nagios-core:1.0"
    build: 
      context: "./"
      dockerfile: "Dockerfile"
    container_name: nagios-eva
    ports:
      - "8080:80"
    restart: always

###   

Este comado buscara la construcciòn declara en el dockerfile,
dockerfile busca la imagen declara a utilizar.

###

> Abrir la url http://localhost:8080/
**utilizar las credenciales de acceso**
Usuario: nagiosadmin
Contraseña: nagios
