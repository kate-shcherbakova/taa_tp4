## M2 IL. TAA TP Keycloak
##### Shcherbakova Kateryna 
##### Tkachenko Oleksii 

Ce projet visait à intégrer Keycloak dans une application Spring Boot. TP était divisé entre le travail sur un projet de démonstration et un projet personnel.

## Partie 1 : projet de démonstration
**Il se trouve dans le dossier `keycloak`.**
### Description

Ce projet utilise Spring Security avec Keycloak pour l'authentification et l'autorisation des utilisateurs. Il présente des contrôleurs configurés pour gérer différentes routes et démontrer l'accès restreint basé sur les rôles des utilisateurs.

### Fonctionnalités

- Authentification basée sur Keycloak
- Autorisation en fonction des rôles utilisateurs
- Gestion de plusieurs endpoints HTTP
- Utilisation de Thymeleaf pour les templates HTML
- Intégration de JWT pour la sécurisation des ressources

### Comment exécuter le projet

1. Assurez-vous d'avoir Java et Maven installés.
2. Configurez Keycloak avec les utilisateurs et les rôles nécessaires.
3. Clonez ce dépôt Git.
4. Configurez les paramètres de connexion à Keycloak dans le projet.
5. Exécuter le fichier `KeycloakApplicationTests`.

### Endpoints

- `/` : Page principale
- `/index` : Page pour les utilisateurs avec le rôle USER
- `/admin` : Page pour les utilisateurs avec le rôle ADMIN

### Technologies utilisées

- Java
- Spring Boot
- Spring Security
- Keycloak
- Thymeleaf
- JWT (JSON Web Tokens)

---

## Partie 2 : projet personnel
**Il se trouve dans le dossier `spring-boot-sample-data-jpa-standalone`.**
### Description
