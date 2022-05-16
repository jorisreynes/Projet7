# Project 7 Openclassrooms Backend Development PHP Symfony

Create an API REST

Made with PHP 7 and Symfony 5

To get a local copy follow these simple steps

git clone https://github.com/jorisreynes/Projet7.git

• Install dependencies

    composer install
    
• Create the database

    php bin/console doctrine:database:create
    
• Create and install migrations

    php bin/console make:migration 

    php bin/console doctrine:migrations:migrate
    
• Create a virtual server

    php -S localhost:8000 -t public


• API information page

    http://localhost:8000/api

• Sign in

 POST method
 
    http://localhost:8000/api/login_check
    
    {
        "username": "test@test.com",
        "password": "password"
    }

•	See product list

GET	method

    http://localhost:8000/api/products

•	See product details

GET	method

    http://localhost:8000/api/products/{id}

•	See the user list of a client

GET method

    http://localhost:8001/api/clients/{id}

•	See the user details of a client
GET	methode

    http://localhost:8001/api/users/{id}

•	Add a new user

POST method

    http://localhost:8001/api/users
    
    {
    "email": "test@test.com",
    "roles": [],
      "password": "test",
      "client": "/api/clients/{id}"
    }

•	Delete an user

DELETE method

    http://localhost:8001/api/users/{id}
