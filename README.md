# CBTA91 ECOMMERCE 🚀
Este proyecto de ecommerce se creo con WordPress y MySQL.

![Captura de pantalla 2024-03-14 a la(s) 1 55 19 p m](https://github.com/EduardoHead18/test/assets/88681044/ef8dae81-cd12-4805-8483-078af94a4590)


## Instalación con Docker <img src="https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white" />
1. Tener instalado Docker.
2. Clonar el proyecto:

`` ➜  ~ git clone repository ``

3. Crear las variables de entorno 1 variable de entorno a raiz del proyecto y una dentro de la carpeta html/.
4. Modificar la tabla wp9o_options en sus campos siteurl y home, cambiamos la url por nuestra url en ambos campos por la url local que es: http://localhost:8007/
5. Si se quiere modificar la cuenta administradora de wordpress podemos encontra la información en la tabla wp9o_options
6. Para crear y correr el contenedor ejecutamos el siguiente comando:

`` docker compose up -d``

5. Cuando se haya creado el contenedor abrimos la url de la aplicación: (http://localhost:8007/)

## Instalación sin Docker en CPanel (Servicio de Hosting). <img src="https://img.shields.io/badge/website-000000?style=for-the-badge&logo=About.me&logoColor=white" />

1. Debemos tener algun proyecto de WordPresss ya creado (vacío).
2. Clonar el proyecto:

`` ➜  ~ git clone repository ``

3. Debemos dirigirnos a nuestro FileManager que nos proporciona el servicio de Hosting que tengamos.
4. Reemplazamos los archivos que se encuentran dentro de la carpeta public o Target por la carpeta html que contiene el repositorio que se clono.
5. Instalar la base de datos: para hacer esto debemos dirigirnos al administrador de base de datos del hosting y corremos el script backup_wordpress.sql que se descargo cuando clonamos el proyecto.
6. Modificar: la tabla wp9o_options en sus campos siteurl y home, cambiamos la url por nuestra url en ambos campos por la url de nuestro dominio.
7. Dentro de la carpeta html existe un archivo llamado wp-config.php, dentro de ese archivo modificaremos la conexión a la base de datos de la siguiente manera:
   
```php
define( 'DB_NAME', 'Nombre de la base de datos' );

/** Database username */
define( 'DB_USER', 'nombre del usuario' );

/** Database password */
define( 'DB_PASSWORD', 'contraseña' );

/** Database hostname */
define( 'DB_HOST', 'host' );
```
6. Listo el proyecto estaria corriendo en nuestro Hosting.

