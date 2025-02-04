
docker run -d \
  -v /var/invoiceninja/public:/var/app/public \
  -v /var/invoiceninja/storage:/var/app/storage \
  -e APP_ENV='production' \
  -e APP_DEBUG=0 \
  -e APP_URL='http://ninja.dev' \
  -e APP_KEY='<APP KEY HERE>' \
  -e APP_CIPHER='AES-256-CBC' \
  -e DB_TYPE='mysql' \
  -e DB_STRICT='false' \
  -e DB_HOST='localhost' \
  -e DB_DATABASE='ninja' \
  -e DB_USERNAME='ninja' \
  -e DB_PASSWORD='ninja' \
  -p '9000:9000' \
  invoiceninja/invoiceninja


docker run -d \
  -v /var/invoiceninja/public:/var/app/public \
  -v /var/invoiceninja/storage:/var/app/storage \
  -e APP_ENV='production' \
  -e APP_DEBUG=0 \
  -e APP_URL='http://ninja.dev' \
  -e APP_KEY='<Wp9/0yGTDcQf3a4SEjlqmwjVj4QrH/Wt7fSOmIbVSIY=>' \
  -e APP_CIPHER='AES-256-CBC' \
  -e DB_TYPE='mysql' \
  -e DB_STRICT='false' \
  -e DB_HOST='10.10.1.16' \
  -e DB_PORT='3306' \
  -e DB_DATABASE='ninja' \
  -e DB_USERNAME='user' \
  -e DB_PASSWORD='password' \
  # -e DB_SSL_ENABLED='false' \
  # -e REQUIRE_HTTPS='false' \
  -p '9000:9000' \
  invoiceninja/invoiceninja