📦 Projeto Laravel – Setup e Execução

Este repositório contém um projeto construído em Laravel.
Siga este guia para rodar o projeto no seu computador de forma simples e rápida.

✅ Requisitos

Antes de tudo, você precisa ter instalado:

PHP 8.1+

Composer

MySQL ou MariaDB

Node.js + NPM

Git

Laravel CLI (opcional, mas recomendado)

📥 1. Clonar o projeto
git clone https://github.com/Vituinho/Projeto-Laravel.git


Depois:

cd Projeto-Laravel

📦 2. Instalar dependências do PHP
composer install

🧰 3. Instalar dependências do front-end (se aplicável)
npm install
npm run build   # ou "npm run dev" para ambiente de desenvolvimento

📄 4. Criar arquivo .env

Crie uma cópia do arquivo de exemplo:

cp .env.example .env


Agora edite o .env e configure sua conexão com o banco de dados:

DB_DATABASE=nome_do_banco
DB_USERNAME=root
DB_PASSWORD=

🔐 5. Gerar a chave da aplicação
php artisan key:generate

🗄️ 6. Criar o banco de dados

No seu MySQL, crie um banco com o mesmo nome do .env:

CREATE DATABASE nome_do_banco;

🧬 7. Rodar as migrations
php artisan migrate


Se o projeto tiver seeders:

php artisan db:seed

▶️ 8. Subir o servidor local
php artisan serve


A aplicação ficará disponível em:

http://127.0.0.1:8000

🛠️ Comandos úteis
Ação	Comando
Limpar caches	php artisan optimize:clear
Rodar migrations novamente	php artisan migrate:fresh
Criar uma migration	php artisan make:migration nome_da_migration
Criar um controller	php artisan make:controller NomeController
🤝 Contribuindo

Sinta-se à vontade para fazer um fork, criar uma branch e enviar um pull request.
