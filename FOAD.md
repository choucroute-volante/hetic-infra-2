# Conception d'une infrastructure sur AWS

Félicitations ! Vous venez de terminer de développer votre nouvelle app (révolutionnaire à n'en point douter) et n'êtes qu'à un déploiement sur AWS d'une longue vie remplie de gloire et de richesses.

Pour y parvenir, vous venez de créer et d'uploader deux images Docker des composants de votre app, appellées **backend** et **frontend** (partez du principe que cette étape est déjà réalisée). Votre application étant révolutionnaire, ces deux images constituent l'intégralité de ce que vous avez à déployer. 


Il ne vous reste plus qu'à designer votre infrastructure et le tour est joué !
Cette tâche peut se décomposer en trois parties 

1. Sélectionner les composants AWS dont vous aurez besoin pour déployer votre app. *(indice: Lisez votre cours et la documentation AWS)*
2. Créer un schéma décrivant l'infrastructure que vous allez déployer *(indice: https://aws.amazon.com/fr/what-is/architecture-diagramming/)*
3. Justifier vos choix techniques (il faut bien convaincre vos futurs investisseurs !)
4. Bonus: Indiquez quel service AWS vous avez utilisé pour uploader vos images Docker et les rendre disponibles dans votre projet AWS

**EXEMPLES DE SCHÉMAS**
- https://farzanaafrintisha.medium.com/basics-of-aws-architecture-diagram-278563b9cfd1
- https://developerck.com/aws-architecture-diagrams/
- https://docs.aws.amazon.com/whitepapers/latest/web-application-hosting-best-practices/an-aws-cloud-architecture-for-web-hosting.html

**CONTRAINTES**
- Vous n'êtes pas à l'aise avec l'administration d'infrastructure, vous opterez donc pour une solution **managée** et **serverless**
- Vous souhaitez que votre application soit déployée sur **deux zones** afin de prévenir à tout désastre naturel pouvant frapper les serveurs (même Jeff Bezos ne peut rien face au dérèglement climatique)

**RENDU**
1. Créez un fichier foad_<nom1>_<nom_2>.md dans votre fork
2. Répondez aux questions et insérez votre schéma dans ce fichier
3. Commitez et pushez ce fichier

Pour insérer une image dans un fichier markdown
https://stackoverflow.com/questions/41604263/how-do-i-display-local-image-in-markdown
https://marinegeo.github.io/2018-08-10-adding-images-markdown/

Pour commit votre rendu:
- git add fichier1 fichier2 ... fichiern
- **n'oubliez pas de commit vos images** pour qu'elles s'affichent dans le ficher en markdown
- git commit -m "message de commit"
- git push
