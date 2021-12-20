<<<<<<< HEAD
# docker-test-britvic-brasil

### Uso

Entre na pasta docker e digite o seguinte comando no terminal:

// docker-compose up -d nginx mysql phpmyadmin

Acessando a workspace:

// docker exec -it test_britvic_workspace_1 bash

### Virtual Hosts

Execute o comando na pasta raíz do projeto para criar o virtual host:

// cp docker/nginx/sites/britvic.conf.example docker/nginx/sites/britvic.conf

Podemos mudar o virtual host no arquivo `britvic.conf` na pasta docker/nginx/sites.

Adicione o virtual host em seu arquivo de host, Exemplo:

// 127.0.0.1 britvic.test

### Criando banco de dados

Acesse o cliente phpMyAdmin para criar seu banco de dados http://localhost:8081/

Banco de dados padrão: test_britvic
Usuário padrão: root
Senha padrão: root
=======
# TESTE BRITVIC BRASIL

## Objetivo

Ajudar a melhor entender o nível de proficiência técnica e de resolução de problemas dos candidatos a
Analista Web para a Britvic. Apresentaremos requisitos que devem ser compreendidos, analisados e
transformados em código funcional.

Os principais critérios analisados serão:

- Cumprimento dos requisitos solicitados;
- Aplicação de boas práticas de desenvolvimento;
- Conhecimento do framework Laravel e suas funcionalidades nativas.

## Requisitos gerais do projeto

Desenvolver um sistema para gerenciar uma locadora de veículos. Deve ser possível listar/criar/editar/remover usuários, assim como veículos. Deve ser possível criar, editar e remover reservas de veículos. Um veículo só pode estar reservado para um usuário por vez. Um usuário pode reservar diversos carros ao mesmo tempo.

Deseja-se uma visão (relatório/tabela) que exiba para um determinado veículo qual a sua reserva/disponibilidade para cada dia de determinado mês.

## Requisitos técnicos

O sistema deve armazenar o nome e o CPF dos usuários, assim como a data e quem foram inseridos no banco de dados.

O sistema deve armazenar o modelo, marca, ano e a placa do veículo.

O sistema deve armazenar as reservas realizadas.

Todos os dados inseridos pelo operador do sistema devem ser validados.

Criar um evento que será disparado quando um carro for reservado. Esse evento deverá escrever no arquivo de log do framework Laravel (utilizando a facade \Log), a id do usuário e a id do veículo reservado.

Criar um Job e programá-lo para execução duas vezes por dia. O método handle do Job pode permanecer vazio.

O repositório deve conter as migrações das tabelas do sistema.

Deve ser observado o padrão MVC.

Deve ser observado o devido tratamento de erros.

Deve ser utilizado o Laravel Mix para compilação de dependências.

Utilize o bootstrap (https://getbootstrap.com/) para construção do front-end.

Utilizar a versão 8 do framework Laravel.

## Orientações

A interface do sistema deve ser a mais simples possível. Concentre-se nos requisitos técnicos e não na estética das páginas. 

É desejável (mas não obrigatório) que o sistema contenha funcionalidade para inserir/remover dados fictícios, para facilitação do teste.

Utilizar o sistema de autenticação do próprio Laravel.

Uso de componentes em Vue JS é desejável.

O uso de bibliotecas terceiras é desejável, desde que respeitados os critérios já citados neste documento.

É desejável que o código seja comentado quando o trecho de código não for óbvio.

É desejável que o repositório contenha Docblocks em todos os métodos.

O projeto deve ser entregue via link de repositório no github.

## Observações
Este é um projeto apenas de teste e não tem envolvimento com a marca Britvic Brasil.
>>>>>>> f2bc87e4b58d1c3414032be70d20e6855fbadd9e
