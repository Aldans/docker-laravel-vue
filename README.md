# Dockerized starter template for Laravel + Vite Vuejs project.

## Pre-requirements

- Docker

```bash
$ docker --version
Docker version 20.10.23, build 7155243
```

- Docker-compose

```bash
$ docker-compose --version
Docker Compose version v2.15.1
```

- Make

```bash
$ make --version
GNU Make 3.81
```

## Stack includes

- php-fpm
- Node.js
- MySQL
- Nginx

## Initial installation

1. Clone this repository.

```bash
$ git clone https://github.com/Aldans/docker-laravel-vue.git
```

2. Running the initial installation.

```bash
$ cd docker-laravel-vue
$ make init
```

3. Install and compile npm packages in running docker container.

```bash
$ cd docker-laravel-vue
$ make node
$ yarn install
$ yarn dev
```

4. Append to the `/etc/hosts` file.

```bash
127.0.0.1 app.loc
127.0.0.1 api.app.loc
```

5. Access to Laravel and Vuejs project.

- Laravel project
  http://api.app.loc

- Vuejs project
  http://app.loc

6. For dev-server ready version need change some things.

- Change variables value in the files `.env` and `docker-compose.yml`
  on environment variables for dev-server.

- Change domain name in all config files from `app.loc`|`api.app.loc` on valid.

- Add SSL certificates for new domain name.
