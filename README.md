# docker-php8.3-mariadb-nginx
<p>This is for running php on docker-windows</p>
<p>-I really don't remember if i make the /app directory</p>
<p>-build the image PHP image with php dependencies with: docker-compose build</p>
<p>-build the container with the networks with: docker compose up</p>

<p>
Firstly i was trying with an rc mariadb version, but it was difficult i couldn't manage errors, so it works with with mariadb:10
</p>

General Purpouse
On APP with laravelRun
docker compose build
docker-compose build

curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
apt-get install unzip
composer create-project laravel/laravel associates-departments-interprise
chown -R www-data:www-data associates-departments-interprise

When the project is created
	apt-get update
	apt-get install -y libpq-dev
	docker-php-ext-install pdo_pgsql

Change DB_Port to 5432
connect to psqldb

	psql -U tutorial_user
	CREATE DATABASE tutorial_db
\l \c

Now you can run
	php artisan migrate:install
	php artisan make:migration
	php artisan migrate --path=database/migrations/20230622093000_create_users_table.php
To make models

	php artisan make:model ModelName -cfsr
	php artisan make:model ModelName -cr
	php artisan make:controller PhotoController --resource
Remember to put App\Http\Controllers\ControllerName on the routes file.

Error on cannot enter logs
	chown -R www-data:www-data storage

JWT Auth Config


Credentials to docker

DB_CONNECTION=pgsql
DB_HOST=psql
DB_PORT=5432
DB_DATABASE=tutorial_db
DB_USERNAME=tutorial_user
DB_PASSWORD=secret_tutorial