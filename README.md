
## Objectif du TP

L'objectif de ce travail pratique est de concevoir et implémenter une architecture microservices complète en utilisant Spring Cloud. Ce projet démontre les concepts fondamentaux des microservices modernes :

- **Service Discovery** : Utilisation de Consul pour la découverte automatique des services
- **API Gateway** : Implémentation d'une passerelle unique pour router les requêtes vers les différents microservices
- **Communication inter-services** : Démonstration de la communication entre services (Car Service communique avec Client Service)
- **Séparation des responsabilités** : Chaque service gère son propre domaine (Clients et Voitures)

### Architecture du Système

Le projet est composé de 4 microservices principaux :

1. **Eureka Server** (Port 8761) : Serveur de découverte de services (optionnel, car les services utilisent Consul)
2. **Client Service** (Port 8088) : Service de gestion des clients avec base de données H2
3. **Car Service** (Port 8082) : Service de gestion des voitures qui récupère les informations des clients via le Gateway
4. **Gateway** (Port 8888) : Passerelle API qui route les requêtes vers les services appropriés en utilisant la découverte de services Consul




Image:

(Screens/2.png)

Cette capture d'écran illustre l'architecture complète du système microservices avec tous les services en cours d'exécution.
Elle montre la communication entre les différents services via le Gateway et leur enregistrement dans Consul pour la découverte de services.

