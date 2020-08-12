![title](https://www.bayonne.cci.fr/images/articles/Le-campus-ESTIA-confirme-son-attractivite_chapeau.png)
# Exercise Proposition Globale Infrastructure

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

