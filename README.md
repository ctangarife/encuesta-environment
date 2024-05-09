# UMEncuestador

Este proyecto es un entorno de desarrollo para una servicio de encuestras

## Requisitos

- docker

## Estructura de carpetas

- build -> Contiene las imagenes custom para el proyecto
- data -> Carpeta que sirve de volumen para el código del proyecto
- db -> Carpeta generada para el volumen de la base de datos
- nginx -> Carpeta con las reglas del servidor

## Instalación

1. Navega al directorio del proyecto: `cd data`
2. En la carpeta data Clona el repositorio: por https `git clone https://github.com/ctangarife/encuesta-node.git` por ssh `git@github.com:ctangarife/encuesta-node.git`
3. Navega al directorio del proyecto: `cd encuesta-node`
4. Instala las dependencias: `npm install`


## Levantar los Contenedores

1. Asegúrate de tener Docker instalado en tu máquina.
2. Ejecuta el siguiente comando para levantar los contenedores: `docker-compose up -d`25

## Uso

- encuesta-pgl -> Contenedor con una base de datos en PGL se accede por el puerto `5437`
- encuesta-nginx -> Contenedor con servidor nginx, para archivos estaticos
- encuesta-nestjs -> Contendor en nestjs con el api del proyecto

