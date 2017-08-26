# Docker Images for Laravel development
[![Docker Build Status](https://img.shields.io/docker/build/jguyomard/laravel-php.svg?style=flat-square)](https://hub.docker.com/r/jguyomard/laravel-php/)
[![Docker Build Status](https://img.shields.io/docker/build/jguyomard/laravel-nginx.svg?style=flat-square)](https://hub.docker.com/r/jguyomard/laravel-nginx/)

This repository provides you a development environment without requiring you to install PHP, a web server, and any other server software on your local machine. For this, it requires Docker and Docker Compose.


## Installation

1. Install [docker](https://docs.docker.com/engine/installation/) and [docker-compose](https://docs.docker.com/compose/install/) ;

2. Copy `docker-compose.yml` file to your project root path, and edit it according to your needs ;

3. From your project directory, start up your application by running:

```sh
docker-compose up
```
4. If you want, you can run composer or artisan through docker. For instance:

```sh
docker-compose exec php composer install
docker-compose exec php php artisan migrate
docker-compose exec php $yourCommandHere
```


## Docker Images

These docker images are configured in `docker-compose.yml` file. 
You can comment or uncomment some services according to your project.

* [`jguyomard/laravel-php:7.1`](https://hub.docker.com/r/jguyomard/laravel-php/) (this docker image extends `php:7.1-fpm-alpine` to add some PHP extensions) ;
* [`jguyomard/laravel-nginx:1.13`](https://hub.docker.com/r/jguyomard/laravel-nginx/) (this docker image extends `nginx:1.13-alpine` to add Laravel vhost) ;
* `mysql:5.7` ;
* `postgres:9.6-alpine` ;
* `redis:4.0-alpine` ;
* `elasticsearch:5.5-alpine`.


## Contributing

Contributions are welcome!
Leave an issue on Github, or create a Pull Request.


## Licence

This work is under [MIT](LICENCE) licence.