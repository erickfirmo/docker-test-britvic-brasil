# docker-test-britvic-brasil

### Clonando o repositório

Digite em seu terminal para clonar o projeto com seus submodulos:

```sh
git clone --recurse-submodules git@github.com:erickfirmo/docker-test-britvic-brasil.git
```


### Uso

Abra a pasta **docker** pelo terminal e digite o seguinte comando:

```sh
cp .env.example .env && docker-compose up -d nginx mysql phpmyadmin
```

Acesse a workspace:

```sh
docker exec -it test_britvic_workspace_1 bash
```

**Nota:** Execute o comando ``composer install`` e os comandos do **artisan** dentro da workspace para instalar o projeto Laravel.

### Virtual Hosts

Execute o comando na pasta raiz deste repositório para criar o virtual host:

```sh
cp docker/nginx/sites/britvic.conf.example docker/nginx/sites/britvic.conf
```

Por padrão, podemos acessar o projeto em http://britvic.test/. Podemos mudar o virtual host alterando a variável de ambiente `server_name` no arquivo `britvic.conf`, localizado na pasta docker/nginx/sites.

```
server_name seu-dominio-local.test;
```

Adicione o virtual host em seu arquivo de hosts. Exemplo:

```
127.0.0.1 britvic.test
```

### Criando banco de dados

Acesse o cliente phpMyAdmin para criar seu banco de dados http://localhost:8081/

**Servidor:** mysql

**Banco de dados padrão:** test_britvic

**Usuário padrão:** root

**Senha padrão:** root
