# Prueba de Marival para aplicar como Full Stack Developer

    En esta prueba tuve que aprender Vue 2.x y Laravel 5.5.x

## Configurar entorno de desarrollo

Para la configuración del entorno de pruebas se usa Docker con el servidor de artisan, para las pruebas de la aplicación.

Habilitar servidor: `php artisan serve --port 80`

Para docker es necesario ejecutar los siguientes pasos:

1. Construir una imagen del archivo `Dockerfile`.
2. Construir un contenedor de la imagen, para que corra en el fondo (background).

```bash
cd database/deploy
docker build -t marival-db:latest .
docker run --name dbserver -d -p 3306:3306 marival-db:latest
```

## Modelo de datos

<p align="center">
    <img src="https://raw.githubusercontent.com/captaincode0/marival-test/master/data-model.jpg" alt="modelo de datos">
</p>

El modelo de datos se compone de las siguientes entidades:

1. Usuarios: Son los administradores del sistema que pueden ejecutar operaciones en el sistema.
2. Session: Son las

## API REST

**Endpoint:** /api/auth

Ruta|Mètodo|Descripción
--|--|--
login|POST|autentica a un usuario en la aplicación siempre y cuando sus credenciales sean correctas.
logout|PUT|termina la sesión de un usuario en la aplicación.

**Endpoint:** /api/auth/sessions

Ruta|Método|Descripción
--|--|--
/|GET|Obtiene todas las sesiones del usuario actual.

**Endpoint:** /api/
