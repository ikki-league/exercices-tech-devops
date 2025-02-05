### Consignes : 
- 🚨 Ceci est un exercice qu'il faut prendre comme une simulation de situation réelle 🚨 
- Nous (IKKI League) nous positionnons en tant que client de la demande énoncée ci-dessous. Vous pouvez nous contacter par e-mail en cas de question(s) sur la problématique à résoudre ci-dessous.

### Contexte :
Nous développons une application web en microservices qui doit être déployée sur une infrastructure cloud. L'application doit être scalable, résiliente, et capable de supporter des pics de charge importants.

#### Partie 1 : Conception d'Architecture 
- **Tâche :** Fournissez un diagramme d’architecture pour une application composée de 5 microservices, dont l'un est critique et doit avoir une haute disponibilité.
  - Les microservices doivent être déployés dans un environnement cloud, en utilisant des conteneurs.
  - Décrivez comment vous géreriez l'équilibrage de charge, le scaling automatique, la tolérance aux pannes et la résilience de votre architecture.
  - Proposez des solutions pour la CI/CD, la gestion des logs, le monitoring et l'alerte.

#### Partie 2 : Automatisation d'une Pipeline CI/CD 
- **Tâche :** Décrivez et mettez en œuvre une pipeline CI/CD basique pour l’un des microservices de l’application.
  - Ce service est une API Node.js.
  - La pipeline doit inclure : 
    1. Un contrôle de la qualité du code 
    2. Une phase de build 
    3. Un déploiement sur un environnement de staging
    4. Un déploiement automatique en production après validation (via approbation manuelle ou automatique).
