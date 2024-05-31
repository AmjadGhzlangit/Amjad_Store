# Amjad Store
This is a web-based eCommerce application built using the (MVC)  architectural pattern

Example Laravel codebase containing real world examples (CRUD, auth, advanced patterns and more) that adheres to the RealWorld spec and API.
This repo is functionality complete — PRs and issues welcome!

Getting started
Installation
Please check the official laravel installation guide for server requirements before you start. Official Documentation

Alternative installation is possible without local dependencies relying on Docker.

Clone the repository

git clone https://github.com/AmjadGhzlangit/Amjad_Store.git
Switch to the repo folder

cd Amjad_Store
Install all the dependencies using composer

composer install
Copy the example env file and make the required configuration changes in the .env file

cp .env.example .env
Generate a new application key

php artisan key:generate
Generate a new JWT authentication secret key

php artisan migrate
Start the local development server

php artisan serve
You can now access the server at http://localhost:8000

TL;DR command list

git clone https://github.com/AmjadGhzlangit/ecommerce-mvc.git
cd ecommerce-mvc
composer install
cp .env.example .env
php artisan key:generate
Make sure you set the correct database connection information before running the migrations Environment variables

php artisan migrate
php artisan serve
Database seeding
Populate the database with seed data with relationships which includes users, articles, comments, tags, favorites and follows. This can help you to quickly start testing the api or couple a frontend and start using it with ready content.

Open the DemoDataSeeder and set the property values as per your requirement

database/seeds/DemoDataSeeder.php
Run the database seeder and you're done

php artisan db:seed
Note : It's recommended to have a clean database before seeding. You can refresh your migrations at any point to clean the database by running the following command

php artisan migrate:refresh
Docker
To install with Docker, run following commands:

git clone https://github.com/AmjadGhzlangit/Amjad_Store.git
cd Amjad_Store
cp .env.example.docker .env
docker run -v $(pwd):/app composer install
cd ./docker
docker-compose up -d
docker-compose exec php php artisan key:generate
docker-compose exec php php artisan migrate
docker-compose exec php php artisan db:seed
docker-compose exec php php artisan serve --host=0.0.0.0
The api can be accessed at http://localhost:8000/api.

Code overview
Dependencies
laravel-cors - For handling Cross-Origin Resource Sharing (CORS)

Environment variables
.env - Environment variables can be set in this file
Note : You can quickly set the database information and other variables in this file and have the application fully working.

Testing
Run the laravel development server

php artisan serve
The api can now be accessed at

http://localhost:8000

