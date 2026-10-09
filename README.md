CodaEats
API de commande de repas (Symfony, API Platform, FrankenPHP, PostgreSQL), servie par Docker.

Installation
Installer Docker Compose (v2.10 ou plus).
make start construit les images, démarre les conteneurs et génère la paire de clés JWT(make jwt, les clés ne sont pas versionnées).
make sf c="doctrine:migrations:migrate -n" applique le schéma, puismake sf c="doctrine:fixtures:load -n" charge les comptes de test.
L'API répond sur https://localhost (certificat auto-signé à accepter) ; la documentation
OpenAPI est sur https://localhost/api/docs.

Les comptes de test sont alice@example.fr, bob@example.fr et camille.aubert@example.fr,
mot de passe motdepasse.

make test lance la suite de tests, make down arrête les conteneurs.
