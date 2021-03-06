
# Controle de Clientes e Pedidos de Compra

Projeto desenvolvido em Laravel e Mysql utilizando ajax e guzzle para requisicoes rest

## O que foi feito/falta ser feito

**Básico:**
-  - [x] Escolha de especialidades
-  - [x] clicar em agendar com médico da preferencia do usuario
-  - [x] preencher dados de agendamento
-  - [x] clicar em solicitar horario
-  - [x] salvar agendamento

**Bônus:**
-  - [x] Acesso aos cadastros de horarios via api (pública)
-  - [x] autenticação de usuario
-  - [x] Area de login com visualização dos agendamentos realizados
-  - Ex resposta: {"id":3,"specialty_id":201,"professional_id":126,"source_id":43,"name":"Wanderson Macedo","birth_date":"2020-03-03","cpf":"14115214716","created_at":"2020-03-12T00:23:45.000000Z","updated_at":"2020-03-12T00:23:45.000000Z"}]


## Instalação

Clone o Repositório(`feegow-challenge`)  

Entre no diretório `feegow-challenge`.

> cd feegow-challenge

Gere o arquivo `.env` baseado no `.env.example`

> cp .env.example .env

> de permissao 777 para o arquivo start_server

"Suba" com o container

> docker-composer up -d --build

Instale as dependências utilizando o `composer`
> docker exec -it devTest_php bash -c "composer install"
> docker exec -it devTest_php bash -c "npm install"
> docker exec -it devTest_php bash -c "npm run dev"

Gere a `APP_KEY` do Projeto
> docker-composer exec php bash -c "php artisan key:generate"

De permissões de escrita e leitura para as pastas dentro de `/storage` 
> chmod -R 777 storage

Crie os Bancos de dados referente a aplicação e aos testes
> docker-composer exec mysql mysql -p
> CREATE DATABASE laravel
> CREATE DATABASE laravel_tests

Configure as variáveis de ambiente no .env
* `DB_` Dados de conexão com o mysql
* `TEST_DB_` Dados de conexão com o mysql para testes unitários

Execute as migrations(se quiser execute com `--seed` que irá executar os seeders)
> docker-composer exec php bash -c "php artisan migrate"



