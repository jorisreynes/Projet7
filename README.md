# Projet7 de la formation Openclassrooms dévéloppement Backend PHP Symfony

Création d'une API REST

Pour télécharger le projet en local

Situez vous dans un répertoire

git clone

Installer les dépendances
composer install

Créer la base de données
php bin/console doctrine:database:create

Créer et installer les migrations
php bin/console make:migration
php bin/console doctrine:migrations:migrate

Créer un server
php -S localhost:8000 -t public

Accéder à la page d'informations de l'API
http://localhost:8000/api

Pour se connecter
POST http://localhost:8000/api/login_check
{
    "username": "test@test.com",
    "password": "password"
}

•	Consulter la liste des produits BileMo
GET	http://localhost:8000/api/products

•	Consulter les détails d’un produit BileMo
GET	http://localhost:8000/api/products/{id}

•	Consulter la liste des utilisateurs inscrits liés à un client sur le site web
GET	http://localhost:8001/api/clients/{id}

•	Consulter le détail d’un utilisateur inscrit lié à un client
GET	http://localhost:8001/api/users/{id}

•	Ajouter un nouvel utilisateur lié à un client
POST	http://localhost:8001/api/users
{
  "email": "test@test.com",
  "roles": [],
  "password": "test",
  "client": "/api/clients/{id}"
}
•	Supprimer un utilisateur ajouté par un client.
DELETE http://localhost:8001/api/users/{id}
