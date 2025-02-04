
## Crear App Key

### Si aún no has iniciado los contenedores, ejecuta:

    $ docker run --rm -it invoiceninja/invoiceninja-debian php artisan key:generate --show

### Si los contenedores ya están en ejecución, ejecuta:

    $ docker-compose exec app php artisan key:generate --show


## Crear el archivo .env

    - Abre o crea un archivo llamado .env en la raíz de tu proyecto Docker Invoice Ninja.

    - Inserta la clave generada en el archivo .env con la siguiente línea:

        APP_KEY=base64encodedstring

    - Asegúrate de reemplazar base64encodedstring con la clave que copiaste en el paso anterior.

