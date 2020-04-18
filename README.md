# Laravel Template Boiler
Basic flow for creating Laravel using Docker-compose.
`
`
This template uses Digital Ocean image for the Laravel PHP.
`
`
`
Steps

1. Git clone latest Laravel at git@github.com:laravel/laravel.git
2. Add .env file or edit .env.example after cloning the Laravel's 
   Since this repo uses Mariadb, set the localhost or DB_HOST to 'db' or whatever name you desire to set in docker-compose.yml.
3. Edit docker-compose.yml by changing the PORT numbers
4. If you have a PHP and Compose running on your local machine, run the docker command
    docker-compose up --build. If not, then just run docker-compose up
5. If you ran docker-compose up then you should be running the composer install command inside your
    container image by running
    docker exec -it {your_laravel_image_app} composer install

6. For JWT auth  follow the procedures from https://jwt-auth.readthedocs.io/en/develop/laravel-installation/
    which basically uses composer install only.

Note: For .env file checkout the APP_SLUG as it will be use in docker-compose.yml file.

