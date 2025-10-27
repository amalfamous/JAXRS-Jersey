# Application JAX-RS avec Spring Boot

## Description
Application de gestion de comptes bancaires développée avec Spring Boot et JAX-RS (Jersey).

## Technologies utilisées
- **Spring Boot** 3.5.7
- **JAX-RS (Jersey)** pour les API RESTful
- **Spring Data JPA** pour la persistance des données
- **H2 Database** (base de données en mémoire)
- **Lombok** pour réduire le code boilerplate
- **Java** 23

## Structure du projet

### Entités
- **Compte** : Représente un compte bancaire avec les attributs suivants :
  - `id` : Identifiant unique
  - `solde` : Solde du compte
  - `dateCreation` : Date de création du compte
  - `type` : Type de compte (COURANT ou EPARGNE)

### Repository
- **CompteRepository** : Interface qui étend JpaRepository pour les opérations CRUD sur les comptes

## Configuration

### application.properties
```properties
spring.application.name=jaxrs
spring.datasource.url=jdbc:h2:mem:banque
server.port=8082
```

## Démarrage de l'application

1. Cloner le projet
2. Ouvrir le projet dans votre IDE
3. Exécuter la classe `JaxrsApplication`
4. L'application démarre sur le port **8082**

## Accès à la base de données H2

- **Console H2** : http://localhost:8082/h2-console
- **JDBC URL** : `jdbc:h2:mem:banque`
- **Username** : `sa`
- **Password** : (laisser vide)

## Test de l'API

### Récupérer tous les comptes
```
GET http://localhost:8082/banque/comptes
```
<img width="1919" height="324" alt="Screenshot 2025-10-27 164352" src="https://github.com/user-attachments/assets/6ad2d25e-1bbf-4e8d-8f13-74ac3476e736" />

```
Accès à la console H2
![WhatsApp Image 2025-10-27 at 16 06 38_944ab7a9](https://github.com/user-attachments/assets/8d19e15b-0c62-4768-9bb1-2620dc597a89)

## Initialisation des données

Au démarrage, l'application crée automatiquement 3 comptes avec des soldes aléatoires :
- 2 comptes EPARGNE
- 1 compte COURANT

## Auteur
[Votre nom]
