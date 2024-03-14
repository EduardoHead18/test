# CBTA91 ECOMMERCE 🚀
Este proyecto de ecommerce se creo con WordPress y MySQL.

![Captura de pantalla 2024-03-14 a la(s) 1 55 19 p m](https://github.com/EduardoHead18/test/assets/88681044/ef8dae81-cd12-4805-8483-078af94a4590)


## Instalación con docker
1. Tener instalado Docker.
2. Clonar el proyecto:

`` ➜  ~ git clone repository ``

3. Crear las variables de entorno.
4. Modificar la tabla wp9o_options en sus campos siteurl y home, cambiamos la url por nuestra url en ambos campos por la url local que es: http://localhost:8007/
5. Si se quiere modificar la cuenta administradora de wordpress podemos encontra la información en la tabla wp9o_options
6. Para crear y correr el contenedor ejecutamos el siguiente comando:

`` docker compose up -d``

5. Cuando se haya creado el contenedor abrimos la url de la aplicación: (http://localhost:8007/)

## Instalación sin Docker en CPanel (Servicio de Hosting).

1. Debemos tener algun proyecto de WordPresss ya creado (vacío).
2. Clonar el proyecto:

`` ➜  ~ git clone repository ``

3. Debemos dirigirnos a nuestro FileManager que nos proporciona el servicio de Hosting que tengamos.
4. Reemplazamos los archivos que se encuentran dentro de la carpeta public o Target por la carpeta html que contiene el repositorio que se clono.
5. Dentro de la carpeta html existe un archivo llamado wp-config.php, dentro de ese archivo modificación modificaremos la conexión a la base de datos de la siguiente manera:
   
```php
define( 'DB_NAME', $db );

/** Database username */
define( 'DB_USER', $dbUser );

/** Database password */
define( 'DB_PASSWORD', $dbPassword );

/** Database hostname */
define( 'DB_HOST', $dbHost );

