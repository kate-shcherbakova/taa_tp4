##### M2 IL. TAA TP Spring
##### Shcherbakova Kateryna 
##### Tkachenko Oleksii 

# Partie 1. Injection de dépendances

Le projet est une application de gestion de magasin développée en utilisant le framework Spring en Java. L'application simule les interactions entre différents acteurs tels que le client, le magasin, la banque et le fournisseur, en offrant des fonctionnalités pour effectuer des opérations d'achat et de gestion de stock. 

## Structure du Projet

Le projet est organisé en plusieurs packages :

- `sample.simple`: Package principal contenant la classe principale de l'application.
- `sample.simple.client`: Contient les classes pour le client et ses interactions avec le magasin.
- `sample.simple.store`: Contient les fonctionnalités du magasin et ses interfaces pour les achats.
- `sample.simple.bank`: Contient les fonctionnalités de la banque pour les transactions financières.
- `sample.simple.provider`: Contient les fonctionnalités du fournisseur pour la gestion des stocks.

## Fonctionnalités Principales

- **Client**: Interagit avec le magasin en effectuant des achats à l'aide des différentes interfaces disponibles (IFastLane, ILane, IJustHaveALook).
- **Magasin**: Offre des fonctionnalités pour vérifier le stock, commander des articles, gérer les paiements et collaborer avec la banque et le fournisseur.
- **Banque**: Gère les transferts d'argent entre comptes pour les transactions liées aux achats.
- **Fournisseur**: Fournit des informations sur les prix des articles et permet de passer des commandes pour réapprovisionner le stock du magasin.

## Utilisation

Pour exécuter l'application :
1. Assurez-vous d'avoir les dépendances nécessaires et Java installé.
2. Importez le projet dans votre IDE.
3. Lancez la classe `SampleSimpleApplication` pour démarrer l'application.

## Injection de dépendances

L'un des principes clés de la conception de ce projet repose sur l'injection de dépendances, qui est utilisée pour gérer les relations entre les composants. L'utilisation de l'injection de dépendances augmente la modularité, la maintenabilité et la testabilité du code.

Le projet utilise l'injection de dépendances de Spring pour connecter les différentes parties de l'application :

- Les composants tels que le client, le magasin, la banque et le fournisseur sont créés en tant que beans Spring, ce qui permet à Spring de gérer leur cycle de vie et leurs dépendances.
- L'annotation `@Autowired` est utilisée pour injecter les dépendances entre les différents composants, permettant ainsi à Spring de connecter automatiquement les différentes parties de l'application.

---

# Partie 2: Spring AOP

Cette partie du projet se concentre sur l'utilisation de Spring AOP (Aspect-Oriented Programming) pour la gestion de la sécurité et le suivi de l'exécution des méthodes. 
L'objectif du projet est d'appliquer l'AOP pour deux fonctionnalités clés : la sécurité et le suivi des méthodes.

## Structure des fichiers
La fonctionnalité AOP a été mise en œuvre dans le projet spring-boot-sample-simple-standalone pour montrer un exemple d'utilisation avec les classes de la partie 1.
- **AOPExecutionLogger**: Aspect pour le suivi de l'exécution des méthodes dans l'application.
- **AOPSecurityAspect**: Aspect pour la gestion de la sécurité avec Spring AOP.
- **SecurityCheck**: Annotation pour marquer les méthodes nécessitant une vérification de sécurité.

## Utilisation
- L'aspect `AOPExecutionLogger` enregistre les appels des méthodes publiques de tous les beans Spring de l'application.
- L'aspect `AOPSecurityAspect` utilise l'annotation `@SecurityCheck` pour contrôler l'accès aux méthodes sécurisées dans l'application, comme illustré dans la classe `Bank`.

---

# Partie 3. Spring-data

Le TP2 a été pris comme base et le framework Spring y a été implémenté. 
Cette application a été conçue pour gérer les informations relatives aux professeurs et aux étudiants dans un environnement éducatif. Elle offre une API RESTful permettant de récupérer des détails sur les professeurs, les étudiants et les rendez-vous.

## Technologies utilisées
- Java
- Spring Framework
- JPA (Java Persistence API)
- HSQL

## Utilisation
1. Exécutez le serveur `run-hsqldb-server.sh`, qui est nécessaire pour la base de données. (En cas de problème, utilisez un serveur avec TAA_TP1.`https://github.com/kate-shcherbakova/taa_tp1`.)
2. Il est également souhaitable d'utiliser le fichier JpaTest du TP1 pour remplir la base de données avec des valeurs initiales.
3. Configurer les informations d'identification de la base de données dans le fichier `application.properties`.
4. Lancer l'application en exécutant la classe principale `RdvApplication.java`.

## Points clés
- Trois entités principales sont gérées : Professeur, Étudiant et Rendez-vous.
- Les controllers pour chaque entité sont exposées via des points de terminaison REST pour récupérer des données spécifiques.

## Endpoints
- **Professeurs** : `/professors`
    - `GET /professors` : Récupère la liste de tous les professeurs.
    - `GET /professors/{id}` : Récupère un professeur par son identifiant.
    - `POST /professors` : Ajoute un nouveau professeur à la base de données.

- **Étudiants** : `/students`
    - `GET /students` : Récupère la liste de tous les étudiants.
    - `GET /students/{id}` : Récupère un étudiant par son identifiant.

- **Rendez-vous** : `/rdvs`
    - `GET /rdvs` : Récupère la liste de tous les rendez-vous.
    - `GET /rdvs/{id}` : Récupère un rendez-vous par son identifiant.

---