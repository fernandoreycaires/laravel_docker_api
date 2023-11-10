# Sistema base em Laravel
### Contem já configurado uma API de usuarios com JWT Token barear e sistema com uma interface Web 

## Tecnologias

- Laravel 10 <br>
- AdminLTE 3.2.0 <br>
- PHP 8.1 <br>
- JWTToken - Tymon JWTAuth 2.0 <br>
- MariaDB 10 <br>
- Docker <br>

## Configurar

> Duplique o arquivo .env.example e renomeie para .env <br>
> Abra-o e coloque as credenciais de sua database <br> 
> Para utilizar a base do Docker utilize a configuração citada abaixo

```php
DB_CONNECTION=mysql 
DB_HOST=db 
DB_PORT=3306 
DB_DATABASE=cliente 
DB_USERNAME=root 
DB_PASSWORD=fer270587 
```

## Baixar bibliotecas

` $ sudo npm install ` <br>
` $ sudo npm run build ` <br>
` $ php artisan migrate ` <br>

> Para instalar as dependencias: 

`$ composer install` <br>

> Para atualizar as dependencias

`$ composer update` <br>

## Docker 

> Para subir a primeira vez o projeto, rode os comandos abaixo

` $ sudo docker compose up --build`  <br>
` $ sudo docker compose exec app php artisan key:generate` <br>
` $ sudo docker compose exec app php artisan migrate` <br>

> Depois acesse pelo browser o localhost


## Alimentar o banco com informações iniciais temporarias

` $ sudo docker compose exec app php artisan db:seed ` <br>

## Informações extras
> O banco de dados que esta configurado na docker esta apontando o armazenamento para docker_components/db/sql/ <br>
> A configuração do servidor HTTP Nginx e do dservidor PHP estão dentro do diretório docker_components, caso necessite de alguma configuração extra <br>
> Tem uma interface grafica para visualização , e também tem a API com autenticação por JWT Bearer<br>
> Os menus criados são apenas para testes, não tem funcionalidades <br>

## Usuario Supremo inicial
> Email: senhor_das_galaxias@nasa.org<br>
> Senha: senhordasgalaxias123<br>
