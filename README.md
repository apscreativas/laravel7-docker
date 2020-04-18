<p align="center"><img src="https://res.cloudinary.com/dtfbvvkyp/image/upload/v1566331377/laravel-logolockup-cmyk-red.svg" width="400"></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/d/total.svg" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

## Información 

Este es un Dockerizado de Laravel + Apache + MariaDB , el cual esta listo para poder lanzar un proyecto iniciarl en Laravel 7

## Requerimientos

 * [Docker]
 * [Docker Compose]
 

## Primeros Pasos 

Debemos de descargar nuestro proyecto en la carpeta que deseemos instalarla : 

    $ git clone https://github.com/apscreativas/laravelmx.git

Todo nuestro código para la creación de Contenedores se encuentra en la carpeta .docker de este proyecto, así pues debemos de entrar a la misma

    $ cd .docker

Para poder correr de manera desantendida y crear todos los contenedores solo debemos correr el siguiente comando 

    $ docker-compose up -d 

## Inicializar Laravel 

Debemos de descargar todas las dependencias y librerias requeridas para LARAVEL. En este paso correremos el contenedor ya listo (CLI) el cual nos permitira correr cualquier comando sobre la carpeta raíz del proyecto. Nuestro CLI ya incluye COMPOSER, PHP y comandos de LINUX para interacturar con dicho contenedor. ES importante hacerles mención que este contenedor solo se crea al momento de ejecutar un comando, destruyendose una vez finalizado el mismo.

Instalar LARAVEL 

    $ docker-compose run cli composer install
    $ docker-compose run cli php artisan key:generate
    $ docker-compose run cli php artisan migrate 
    
## Detener Dockerizado (Contenedores)

Estando dentro de la carpeta .docker de nuestro proyecto solo debemos correr el siguiente comando 

    $ docker-compose down

## Licencia

Laravel framework es un codigo abierto sobre la licencia.  [MIT license](https://opensource.org/licenses/MIT).


## Contacto

@davidportales
ventas@apscreativas.com 

