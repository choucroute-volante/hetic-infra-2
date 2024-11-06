# Conception et Déploiement d'une Infrastructure Cloud Sécurisée avec AWS

## Objectifs :
Ce TP a pour but de vous familiariser avec les bases de la conception d'infrastructures en utilisant des technologies de conteneurisation et de déploiement sur le cloud. Vous apprendrez à conteneuriser une application web, à la déployer sur AWS, et à mettre en place des mesures de sécurité de base, telles que la gestion des droits d'accès.


### Partie 0: Récupération du code source
- Créer un fork de ce repo: https://github.com/choucroute-volante/hetic-infra-2
- Y créer un fichier binome.md en y ajoutant les noms et prénoms de vos binômes, puis commit et push ces modifications.


### Partie 1 : Conteneurisation d'une Application Web

#### Récupération et lancement de l’app :
- Lancer l’application et vérifier son bon fonctionnement

#### Création du Dockerfile :
- Écrire un Dockerfile pour conteneuriser l'application.

#### Construction et Test de l'Image :
- Construire l'image Docker localement 
- Tester l'image en exécutant le conteneur localement pour vérifier que l'application fonctionne correctement.

### Partie 2: Veille Techno

- Lire, analyser et résumer ces trois articles:
    - https://www.softfluent.fr/blog/microservices/
    - https://datamyte.com/blogs/infrastructure-scaling/
    - https://www.redhat.com/en/blog/cloud-vs-on-premises

### Partie 3 : Déploiement sur AWS avec Fargate

Mise en place du plan d'infra réalisé hier.
Vous devez déployer, grâce à des services ECS provisionnés par Fargate, une app web simple. Pour simplifier le processus, nous n'uploaderons pas d'image Docker mais travaillerons avec celle de l'Ingress Controller NGINX (image = nginx:latest)
Déployez sur AWS un déploiement contenant deux replicas de conteneurs basés sur cette image.

**CONTRAINTES**
- Déployez votre app sur deux AZ
- Vos machines faisant tourner les conteneurs ne doivent pas être directement accessibles depuis Internet

**INDICES**
- N'oubliez pas de créer des NAT Gateways
- Vérifiez dans quels subnets votre équilibreur de charges a été déployé
- Vérifiez que votre pare-feu est bien configuré pour accepter le trafic entrant
- Pour accéder à votre app, demandez vous quel composant relie votre projet au reste d'internet, et par conséquent quel composant possède un record DNS (un nom lisible par un humain) 

**RENDU**
- Des captures d'écran de votre infrastructure
- Si possible de votre navigateur montrant l'URL de votre site accompagné du message de bievenue du controlleur nginx.

**/!\ IMPORTANT**
- Lorsque vous avez terminé votre TP et collecté les screenshots montrant votre avancement, n'oubliez pas de supprimer toutes les ressources créées, **EN PARTICULIER LA OU LES NAT GATEWAYS**, qui sont facturées 0.05€/instance/h

#########################################################################################################################################################

## Livrables :
Le Dockerfile et tout autre fichier de configuration nécessaire.
Les captures d'écran prouvant le bon fonctionnement de l'application déployée sur AWS.
Votre plan d'infra, comprenant schémas et motivations techniques (FOAD)
