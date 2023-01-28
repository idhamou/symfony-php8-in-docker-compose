
# Symfony 6 + PHP 8.0.13 with Docker

**ONLY for DEV, not for production**

## Run Locally

Clone the project

```bash
  git@github.com:idhamou/symfony-php8-in-docker-compose.git
```

Run the docker-compose

```bash
  docker-compose build
  docker-compose up -d
```

Log into the PHP container

```bash
  docker exec -it php8-sf6 bash
```

Create your Symfony application and launch the internal server

```bash
  symfony new your-project-name --full
  cd your-project-name
  symfony serve -d
```

Create an account (identical to your local session)

```bash
  adduser username
  chown username:username -R .
```

*Your application is available at http://127.0.0.1:9000*

If you need a database, modify the .env file like this example:

```yaml
  DATABASE_URL="postgresql://symfony:ChangeMe@database:5432/app?serverVersion=13&charset=utf8"
```

## Ready to use with

This docker-compose provides you :

- PHP-8.0.13-cli (Debian)
    - Composer
    - Symfony CLI
    - and some other php extentions
    - nodejs, npm, yarn
- postgres:13-alpine
- mailcatcher


## Requirements

Out of the box, this docker-compose is designed for a Linux operating system, provide adaptations for a Mac or Windows environment.

- Linux
- Docker
- Docker-compose
## Author

- [@idhamou](https://github.com/idhamou)
