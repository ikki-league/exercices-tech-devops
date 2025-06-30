
   A propos du contexte, à quel type d'utilisateurs s'adressent les applicatifs ? Font-il partie de l'organisation interne (dans ce cas, quel(s) sont les entités utilisatrices ?) ou plutôt d'un public externe ?
   
Il y a trois types d'utilisateurs pour notre solution de réservation en ligne de billet de curling: 
- Des internautes
- Des administrateurs de la solution (employés chez nous mais opérant au sein de l'entreprise ou chez eux. De ce qu'il m'a été remonté dernièrement il y aura deux front: 1 pour les internautes et un pour les administrateurs qui lui ne serait pas exposé sur internet)
- Des applications qui vont consommer nos services ou pousser de la donnée



- Des applications qui vont consommer nos services ou pousser de la donnée



Bonjour monsieur Kaloudoff,

Mes réponses en rouge. 


Nous supposons ici que l'application que vous développez est basée sur un protocole https, avec pour cible à la fois des postes de travail classiques et des terminaux mobiles type tablette et téléphone.

L'application que nous développons doit fonctionner effectivement sur plusieurs devices. 

Aussi, dans ce contexte, nous ajouterons automatiquement une API Gateway qui aura pour rôle:

- de simplifier les appels aux microservices de votre application via une API unifiée.
- d'aiguiller les flux entre les services
- d'assurer une conversion éventuelle lorsque nécessaire (accès à des données sérialisées). 
- de gérer la partie "Identity and Authentication Management" (IAM)

Concernant l'API Gateway, quels sont les coûts associés à la mise en place de ce composant (financier / humain / technique). Notre budget étant limité nous ne souhaitons pas alourdir la solution avec un composant complémentaire. 

A ce propos, parlez-nous s'il vous plaît de vos contraintes tant en matière d'authentification qu'en matière de gestion des accès;
- côté utilisateur (authentification Google, Facebook par exemple),
- côté administrateur (quelle brique sso ?)
- pour les applicatifs tiers

L'équipe technique m'a parlé d'un composant qui s'appelle Keycloak qui servirait a l'authentification des appels API et des utilisateurs. 

Nous pourrons ainsi vous proposer des solutions en phase avec vos besoins et le type d'hébergement retenu.

Pour l'hébergement des services cloud, avez-vous une préférence pour le Cloud provider ? (OVHCloud, Linode, AWS, Azure, GCP, etc.)

AWS, nous avons d'ailleurs certaines apis qui vont alimenter la solution hébergé sur ce cloud provider. 

En ce qui concerne l'accès aux données par l'intermédiaire d'applications tierces,  les échanges de données peuvent se produire de manière synchrone ou asynchrone (batch, streaming ..) . 

Cela dépendra du service consommé, je pense qu'on aura très probablement les deux cas, c'est a dire que certaines données auront besoin d’être rafraîchies quotidiennement alors que d'autres nécessiteront du temps réel. 

Le mode asynchrone permet en particulier de palier de rendre fluide et fiable l'exploitation de la solution même lorsque l'un des partenaires rencontre une indisponibilité prolongée.
