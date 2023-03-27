# This Config for Laravel

# Docker Conversion
## Do step by step
### Copy `.env.example` to `.env`
## Put Env Variables in the .env
- `DB_HOST=mysql_db`
This might be update with the docker MySQL service's network
- `DB_DATABASE=<<your_desire>>`
- `DB_USERNAME=<<your_desire,not_root_user>>`
- `DB_PASSWORD=<<your_desire>>` 

Above DB configuration will create new database and dbuser automatically accourding to your configuration.
#####
- `HOST_UID=1000`
- `HOST_GID=1000`
- `WEB_PORT_HTTP=80`
- `WEB_PORT_SSL=4433`
- `DB_EXTERNAL_PORT=33066`
- `PMAHOST_PORT=8888`

## Docker
- docker-compose -f docker-compose.yml build 
- docker-compose -f docker-compose.yml up -d
### Enter Docker Container
- docker exec -it `<< Docker Name >>` bash
- `cd /path_to_project/`
- composer update
- php artisan key:generate
- php artisan cache:clear
## Running Project
- Browser URL : `localhost: <<WEB_PORT_HTTP>>`
<i>Example ; localhost:8080</i>