# Serveur

## Dépendances

Le client nécessite la version 11 de Java ou supérieur.
La gestion des dépendances passe par Gradle. Le script de lancement de ce dernier est dans le dépôt.

Les données sont stockées dans un SGBD relationnel : Apache Derby. 
Celui-ci est inclus dans le projet et ne nécessite pas de configuration pour pouvoir se lancer.

Il est nécessaire de posséder une file RabbitMQ pour lire les messages du serveurs.
La communication se fait par ce moyen.

## Configuration

Il est possible de changer la file rabbitMQ en modifiant le fichier : [src/main/resources/application.yml](src/main/resources/application.yml)

## Utilisation

Pour être lancé, il nécessite de passer par gradle.

```./gradlew bootRun```

Pour répondre au besoin du projet, des données sont déjà mises dans l'application. 
Celle-ci permettent de faire des requêtes dans l'application de manière simple.

(Optionnel)
Il est possible de compiler l'application indépendamment via la commande :

    ./gradlew build

## Test

Des tests fonctionnels sont présents au sein de l'application. Ils sont dans le dossier [src/test/java/eu/telecomnancy/projetsdis/server/](src/test/java/eu/telecomnancy/projetsdis/server/).
Pour les lancer, il faut lancer la commande :

    ./gradlew check

## Liste des routes disponibles

Elles sont présentes dans les fichiers 

- [doc/listeRoute/Personne.md](doc/listeRoute/Personne.md) 
- [doc/listeRoute/Equipe.md](doc/listeRoute/Equipe.md) 
- [doc/listeRoute/Lien.md](doc/listeRoute/Lien.md) 