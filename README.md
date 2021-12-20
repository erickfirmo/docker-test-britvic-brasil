# docker-test-britvic-brasil

### Uso

Entre na pasta **docker** e digite o seguinte comando no terminal:

```sh
cp .env.example .env && docker-compose up -d nginx mysql phpmyadmin
```

Acessando a workspace:

```sh
docker exec -it test_britvic_workspace_1 bash
```

**Nota:** Execute o comando ``composer install`` e os comandos do **artisan** dentro da workspace para instalar o projeto Laravel.

### Virtual Hosts

Execute o comando na pasta raiz deste repositório para criar o virtual host:

```sh
cp docker/nginx/sites/britvic.conf.example docker/nginx/sites/britvic.conf
```

Podemos mudar o virtual host no arquivo `britvic.conf` na pasta docker/nginx/sites, alterando a variável `server_name`.

```
server_name seu-dominio-local.test;
```

Adicione o virtual host em seu arquivo de host, Exemplo:

```
127.0.0.1 britvic.test
```

### Criando banco de dados

Acesse o cliente phpMyAdmin para criar seu banco de dados http://localhost:8081/

**Servidor:** mysql

**Banco de dados padrão:** test_britvic

**Usuário padrão:** root

**Senha padrão:** root
