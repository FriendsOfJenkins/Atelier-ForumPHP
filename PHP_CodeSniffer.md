# Utilisation de Jenkins & PHP_CodeSniffer

## Installation de Jenkins

Il faut tout d'abord vérifier que Java est installé : *java -version*

J'ai opté pour une installation via l'installeur OSX. C'est un package qui va ensuite copier *jenkins.war* dans */Applications/jenkins*.

Puis je lance Jenkins avec la commande suivante :
*java -jar /Applications/jenkins/jenkins.war*

Jenkins est alors normelement accessible à l'URL : [http://localhost:8080](http://localhost:8080)

## Installation de PHP_CodeSniffer

J'ai téléchargé PHP_CodeSniffer manuellement depuis le site de PEAR. Je peux son fonctionnement en exécutant la commande *phpcs* présente dans le dossier *scripts* du projet.

## Lancement d'un 1er test à la main

Je lance la commande *phpcs (dossier du projet à vérifier)* et j'obtiens bien un résultat de test avec une configuration de PHP_CodeSniffer par défaut.

## Créer un job dans Jenkins

Je créé un Job basique en choisissant un *projet free-style*.

Sa configuration est assez simple :  
- Aucune gestion de code source  
- Exécution d'un script shell

Le script shell que j'exécute est le suivant :  
*/(chemin jusqu'à PHP_CodeSniffer)/scripts/phpcs (chemin jusqu'à mon projet à vérifier)*