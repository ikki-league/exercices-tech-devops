
Vous devez déployer une application web classique en JavaScript dans une infrastructure Docker Swarm. L'application doit être capable de se connecter à une base de données PostgreSQL et de s'exécuter sur plusieurs nœuds Docker.

Voici les étapes à suivre pour mener à bien l'exercice :

1. Configurer l'application pour qu'elle fonctionne correctement dans l'infrastructure Docker Swarm. Veillez à prendre en compte les points clés suivants :
- L'application doit être conçue pour s'exécuter sur plusieurs nœuds Docker.
- L'application doit être capable de se connecter à une base de données PostgreSQL.

2. Mise en place de l'infrastructure :
- Créer un cluster Docker Swarm avec plusieurs nœuds.
- Configurer un service Docker pour l'application web, en utilisant l'image Docker de l'application.
- Configurer un service Docker pour la base de données PostgreSQL, en utilisant l'image Docker de PostgreSQL.

3. Automatisation et déploiement continu :
- Utiliser Git pour gérer le code source de l'application.
- Configurer un pipeline CI/CD pour automatiser le processus de construction et de déploiement de l'application sur le cluster Docker Swarm.
- Utiliser Docker Compose pour déployer l'application localement et vérifier que tout fonctionne correctement.

4. Surveillance et sauvegarde :
- Utiliser des outils de surveillance Docker pour surveiller l'état des nœuds Docker et des services.
- Configurer des sauvegardes régulières de la base de données PostgreSQL pour garantir la disponibilité des données en cas de sinistre.
