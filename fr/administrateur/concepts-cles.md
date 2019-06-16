---
title: Concepts clés
lang: fr
role: admin
ref: key-concepts
---

# Tâches et livraisons

Les tâches sont les plus petites unités de travail sur la plateforme.\\
Une tâche est **une action à effectuer à une adresse géographique, sur un créneau horaire défini**.\\
Il existe deux types de tâches différentes :
- **Récupérer**, pour un retrait de marchandise
- **Déposer**, pour un dépôt de marchandise

Une livraison est composée d’au moins deux tâches. Dans une livraison l'ordre des tâches est imposé (classiquement récupérer avant de déposer).

### Attributs d'une tâches

Le livreur doit récupérer une marchandise à une adresse et l’amener à une autre adresse.\\
Les informations suivantes doivent être renseignées par le dispatcheur pour chaque tâche :
- Créneaux
- Adresse
- Commentaire

Les informations suivantes permettent de suivre l’évolution d’une tâche dans le processus de livraison :
- Statut
- Historique

# Instance CoopCycle

Le logiciel CoopCycle fonctionne grâce au déploiement d’instances. Ces dernières sont des copies répliquées du logiciel qui sont autonomes les unes des autres. Cela permet à chaque coopérative d'avoir ses propres règles de tarification, son espace de dispatch et de configurer le logiciel selon ses besoins. Les données (clients, coursiers, commandes) sont isolées entre chaque instance.

### Les rôles dans les instances

Chaque instance dispose de rôles pour ses utilisateurs :
- Administrateur
- Coursier
- Restaurant
- Magasin
- Client

À ces rôles sont assignés des permissions dans la plateforme. Voir la section [Utilisateurs](/fr/administrateur/utilisateurs.html) de la documentation pour plus d'informations.
