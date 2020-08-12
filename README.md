![title](https://www.bayonne.cci.fr/images/articles/Le-campus-ESTIA-confirme-son-attractivite_chapeau.png)
# ExercisePropositionGlobaleInfrastructure

Elaboré par: Virginia PEREZ  
ESTIA - Bidart; 
23 Juillet 2020.

Cette mise en situation professionnelle reconstituée à pour objectif la validation des compétences du bloc "Mettre en ouvre l'intégration continue" à fin de mantenir un système stable pour la sociète MASSIVE DATA.

L'API data-retriever developpés par MASSIVE DATA, c'est une "application programming interface" qui permet l'interaction, la connexion entre les applications des données et les systèmes de service, elles sont comme un "pont" entre les deux. Cette API est un service qui permet de recolter des donnes au pres des adresses https et renvoyer une reponse a travers la même API. Ensuite ces données pourront être visualisés dans des tableaux de bord developpés par la sociète Massive Data.

![alt text](https://qatestlab.com/assets/Uploads/API-Application-Programming-Interface.jpg)

## 1. Analyses de la situation actuelle

MASSIVE DATA a deux processus de livraison que par fois sont disjoints. Ces deux processus sont:

    1. La creation des applications API,
    2. L'evolution de la plateforme MASSIVE DATA -PLATFORM.
    
Dans le tableau suivant on as détaillé les possibles causes et propositions préliminaires ainsi que des outils.


|Problématique        |Possibles causes de la problematique           |Proposition preliminaire des outils                          |
|---------------------|----------------------------------------|--------------------------------|
|Version d'application ne sont plus compatibles entre elles.|Veilles technologiques pas regulières, Pas de creation d'un environnement clos.           |Backlog, GIT, Docker.                    | 
|Les clients trouvent des bugs avant nous.      |Test manuels et unitaires insuffisants et pas très précise avant livraison.  | TDD Test Driven Developpement, Revue de code, Processus de livraison à ameliorer, SquashTM, Atlassian Jira ou Bamboo, GITLab, Azure, Postman, Mantis,Plans d'Assurance Qualité PAQ.|
|Nous ne sachions plus ce qui a été livré pour communiquer au client.|Des Backlog du produit et du sprint qui ne sont pas suivies.    |Atlassian, GITLab, Azure.|
|Les equipes passent des heures à déployer les solutions.            |Une strategie de livraison pas adapté.  Abscence de transversalite dans les équipes, Abscence de formation continue, accumulation des refactoring. |  Atlassian Bamboo ou Jira, Azure Stack HCI et Azure DevOps, GITLab, GitHub|
|Les documentations sont toujours obsolètes.| Personnel pas suffiçant par rapport à la charge de travail.| Slate, formations en docstring, doctest, Markdown. |

UML - Diagramme de clases. Dans lequel on peut approfondir et definir le cahier de charge.

![image.png](attachment:image.png)

## 2. Mise en place d'un environnement technique adapté

Dans ce premier audit on a pu faire une recommandation préliminaire. La plupart des outils recommandées seront décrit à continuation :

### 2.1. IDE Integrated Developpement Environnement

Un IDE un environnement de programmation complet qui se présente sous la forme d'une application.

Il permet de s'assurer que les développeurs ont les bons outils pour être plus efficaces. 

Il est composé généralement d'un éditeur de code, d'un compilateur, d'un débogueur et d'un générateur d'interface graphique. Ils existent plusieurs IDE dans le cadre de l'intégration continue

![2020-08-12_logos](D:/Documents/ESTIA/Evaluation/images/2020-08-12_logos.png)

![title](https://www.bing.com/images/search?view=detailV2&insightstoken=bcid_RINKFUZrIasBsFIauoTs6UhEXqFO.....2g*ccid_g0oVRmsh&form=ANCMS1&iss=SBIUPLOADGET&selectedindex=0&id=-1447088696&ccid=g0oVRmsh&exph=127&expw=600&vt=2&sim=11)

![alt-text](C:/Users/luzan/estia/estia_fichierexample/2020-08-12_logos)





On propose de travailler avec Visual Studio code parce que il s'adapte à la plus part des langages de programmation.

### 2.2. Integration et Livraison Continue CI/CD

L'integration et la livraison continue des logiciels c'est un processus complexe qui requiere plus que simplement appuyer sur un bouton ou deux.

Pour assurer que les versions d'application soient suivies et bien testés avant d'être mises en production, C'est recommandable d'utiliser des outils que permettront l'orchestration de l'intégration et de la livraison continue (CI/CD) appropiées.

Aujourd'hui, existent plusieurs platformes qui permettent de travailler avec, Atlassian Jira, Atlassian Bamboo, GitLab, AzureDevOps, Jenkins X Pipelines, circleCI, Tuleap, etc.

A continuation vous verrez celles qu'on as regardé dans une première révision.

#### 2.2.1. Atlassian Jira Software - Jira Service Desk - Confluence - Bitbucket - Trello

Atlassian Jira, c'est un excellent approche agile tres agreable pour planifier et developper son produit. On peut définir plusieurs projets avec Jira Service Desk, bitbucket on as une synchronisation des commits, gerer des tickets avec Jira Software, Trello pour presenter les backlogs pour definir les stories, Jira conformance avec plus de 77 configurations pour suivre les projets par rapport a son contexte,  etc.

![image.png](attachment:image.png)

![image.png](attachment:image.png)

Chaque projet peut être parametrisé.

Par example, pour la feuille de route, les projets peuvent être géres grâce aux epics, les avancements sont visualisés afin que tout l'équipe soit dans la même longueur d'onde.

![image.png](attachment:image.png)

L'outil de ticketing est excellent pour gérer les incidents des differentes versions. Chaque ticket peut donner un degré d'information précis ( descriptions, niveau de gravité, captures d'écran, etc). Les bugs sont classez et hiérarchisés.

![image.png](attachment:image.png)

![image.png](attachment:image.png)

#### 2.2.2. Atlassian Bamboo

Atlassian Bamboo est un serveur de CI/CD qui peut fournir:

* Automatise la gestion des versions des applications logicielles. avec un marquage des versions.
* La construction et les test automatisés du code source.
* Des mise à jour sur les builds qui ont réussi et échoués.
* Des outils de reporting pour l'analyse statistique.
* Crée des pipelines de livraison continue pour partager des artifacts plans buildés dans un environnement de déploiement. 
* Les déclencheurs sont créés en fonction des modifications détectées dans le référentiel. Pousse les notifications de Bitbucket, un calendrier défini, l'achèvement d'une autre build ou toute combinaison de ceux-ci.

![image.png](attachment:image.png)

![image.png](attachment:image.png)

Vous pouvez prendre un instantané de vos artefacts depuis une compilation réussie dans une version.

Ensuite, vous pouvez déployer le projet, annuler et/ou promouver les versions dans les environnements de development, de staging ou de production.

Suivez quoi, quand et qui a déployé des versions dans vos environnements.

![image.png](attachment:image.png)

#### 2.2.3. GitLab

Propose aussi une plateforme agreable collaborative qui permet de faire de la CI/CD: activer des build automatisés, d'exècuter des tests, déployer du code à chaque validation ou push, gestion, suivi des problèmes, analyses et un wiki.

Il est supporté sur Linux(Ubuntu, Debian), CentOS, Oracle Linux.

![image.png](attachment:image.png)

![image.png](attachment:image.png)
