# Adonis 5 - criando uma API com a versão oficial - Code/Drops #71
Criando uma API com a versão 5 do Adonis com a Daniele Leão

[![Run in Insomnia}](https://insomnia.rest/images/run.svg)](https://insomnia.rest/run/?label=Adonis%20V5&uri=https%3A%2F%2Fraw.githubusercontent.com%2Fdeibsoncogo%2FAdonisV5%2Fmaster%2FInsomnia-All_2022-03-08.json)

## Comandos
Usamos este comando para criar o projeto, logo depois selecionamos que o projeto será do tipo `api`
```bash
yarn create adonis-ts-app adonisv5
```

Para executar a aplicação utilizamos o atalho `yarn dev` ou o comando abaixo
```bash
yarn node ace serve --watch
```

Para criar um controller utilizamos o seguinte comando
```bash
node ace make:controller User
```

Para criar uma migration utilizamos o seguinte comando
```bash
node ace make:migration users
```

Para executar as migrations utilizamos o seguinte comando
```bash
node ace migration:run
```

Para criar o model utilizamos o comando abaixo
```bash
node ace make:model User
```

Para criar o model junto da migration utilizamos este comando
```bash
node ace make:model User -m
```

### Banco de dados
Primeiro temos que instalar a dependência `lucid`
```bash
yarn add @adonisjs/lucid
```

Depois informar qual tipo de banco de dados que iremos utilizar, neste caso foi utilizado o `Postgres` e comandos no `terminal`
```bash
node ace configure @adonisjs/lucid
```

Para criar o container do `Docker` utilizamos este comando
```bash
docker run --name AdonisV5 -e POSTGRES_DB=adonisv5DB -e POSTGRES_USER=adonisv5 -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres
```

Por último configurar o arquivo `.env` conforme informações inserida do comando acima
```bash
DB_CONNECTION=pg
PG_HOST=localhost
PG_PORT=5432
PG_USER=adonisv5
PG_PASSWORD=docker
PG_DB_NAME=adonisv5DB
```
