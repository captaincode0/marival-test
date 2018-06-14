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



