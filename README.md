
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
illustre l'architecture complète du système microservices avec tous les services en cours d'exécution.


<img width="1920" height="1017" alt="2" src="https://github.com/user-attachments/assets/3038d7f3-d525-431b-8be3-53e9af5f96b7" />


