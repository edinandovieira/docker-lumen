
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

## Conectando ao banco de dados

Após a instalação do seu laravel e testar seu localhost, você deverá alterar seu arquivo .env para que sua aplicação reconheça o banco.

O detalhe desta vez esta nos paramêtros, no arquivo docker-compose.yml configuramos os dados abaixo que são necessários alterar no .env

```bash
 - MYSQL_PASSWORD=P@ssword
 - MYSQL_USER=Us&r
 - MYSQL_DATABASE=Db
```

No .env trocamos para, o único detalhe é que no DB_HOST precisamos alterar para o mesmo nome do Service de banco de dados que colocamos no docker-compose.yml

```bash
  DB_CONNECTION=mysql
  DB_HOST=db
  DB_PORT=3306
  DB_DATABASE=Db
  DB_USERNAME=Us&r
  DB_PASSWORD=P@ssword
```