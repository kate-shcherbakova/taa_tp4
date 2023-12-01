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
Le but de cette partie était d'intégrer Keycloak dans un projet personnel. Ce projet est une application Spring qui gère les rendez-vous entre les étudiants et les professeurs.

### Comment exécuter
Pour exécuter ce projet :
1. Assurez-vous d'avoir Java et Maven installés.
2. Configurez Keycloak avec les utilisateurs et les rôles nécessaires .
3. Clonez ce dépôt Git.
4. Configurez les paramètres de connexion à Keycloak dans le projet.
5. Exécuter le fichier `RdvApplication.java`.

### Intégration de Keycloak
Keycloak a été intégré au projet en effectuant les étapes suivantes. 
1. Configuration du Realm dans Keycloak
    - Créez un nouveau Realm dans Keycloak via l'interface d'administration (`http://localhost:8080/admin/<test>/console/`).
    - Ajoutez les clients, utilisateurs et rôles requis pour votre Realm.
2. Configuration de Spring Security
    - Ajoutez les dépendances Keycloak nécessaires à votre projet Spring Boot. Les URL des serveurs Keycloak ont été ajoutées au fichier `application.properties`. 
    - Configurez SecurityConfig pour spécifier les rôles autorisés pour chaque endpoint. Ces paramètres ont été mis en œuvre dans le fichier `SecurityConfig.java`.
    - Assurez-vous que Spring Security gère correctement les demandes d'authentification en utilisant les tokens JWT de Keycloak.
3. Test de l'intégration
    - Démarrez votre application.
    - Testez l'accès aux différents endpoints en utilisant les utilisateurs configurés dans Keycloak avec les rôles associés. 
    
### Vérification
Pour vérifier le bon fonctionnement de Keycloak, un jeton JWT a été obtenu à l'aide de la commande cURL suivante :
```
curl --location 'http://localhost:8080/realms/springbootpersonalrealm/protocol/openid-connect/token' \
--header 'Content-Type: application/x-www-form-urlencoded' \
--data-urlencode 'username=<test>' \
--data-urlencode 'password=<test>' \
--data-urlencode 'grant_type=password' \
--data-urlencode 'client_id=<test>' \
--data-urlencode 'client_secret=<test>' \
--data-urlencode 'scope=openid'
```
Cela permet d'obtenir un jeton JWT qui peut ensuite être utilisé pour l'authentification et l'autorisation. Ce jeton contient des informations sur l'utilisateur, les rôles et les autorisations.

Le jeton reçu peut être utilisé pour accéder aux ressources protégées de l'application :

```
curl -i -X GET http://localhost:8081/test-endpoint \
-H "Authorization: Bearer <TOKEN>"
``` 

### Endpoints
- `/students` : Page pour obtenir tous les étudiants avec le rôle USER et ADMIN
- `/professors` : Page pour obtenir tous les professeurs avec le rôle USER et ADMIN
- `/rdvs` : Page pour obtenir tous les rendez-vous avec le rôle ADMIN

---
