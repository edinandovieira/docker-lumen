
# Docker com Lumen, Nginx e MySQL

Repositório para simplificar a criação de um ambiente com Lumen Framework




## Clonar Repositório

```bash
  git clone https://github.com/edinandovieira/docker-lumen.git
  cd docker-lumen
```
## Docker Composer

Rode o comando abaixo para deixar os containers rodando

```bash
  docker-compose up -d
```
## Instalando o Lumen

Dentro do terminal acesse o seu container php

```bash
  docker exec -it php /bin/bash
```

Agora ja dentro do container executamos o comando do Lumen

```bash
  composer create-project --prefer-dist laravel/lumen projetoteste
```
## Testando a aplicação

Acesse a página no navegador

```bash
  http://localhost/public/
```