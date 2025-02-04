
## CREATE CONNECTION & DATABASE

    - Se debe de crear una base de datos en MySQL o MariaDB para Invoice Ninja


## CERTIFICADO SSL

    - Invoice Ninja exige que la base de datos tenga SSL

### Crear certidicado SSL

    $ sudo openssl req -new -newkey rsa:2048 -nodes -keyout /etc/mysql/ssl/server-key.pem -out /etc/mysql/ssl/server-cert.pem


### Crea la carpeta ssl si no existe

    - Si da error el paso anterior puede ser debido a que la carpeta no esta creada

        $ sudo mkdir -p /etc/mysql/ssl/


### Configura MySQL para usar SSL:

    - Edita el archivo de configuración de MySQL (/etc/mysql/mysql.conf.d/mysqld.cnf) y agrega las siguientes líneas:

    [mysqld]
    ssl-ca=/etc/mysql/ssl/ca-cert.pem
    ssl-cert=/etc/mysql/ssl/server-cert.pem
    ssl-key=/etc/mysql/ssl/server-key.pem

### Reinicia el servicio MySQL para aplicar los cambios:

    $ sudo systemctl restart mysql


### Verifica la configuración:

    - Conéctate a MySQL y verifica que SSL esté habilitado:

        $ mysql -u andresgiraldo -p SHOW STATUS LIKE 'Ssl_cipher';


