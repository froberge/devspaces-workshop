# Introduction to Red Hat Code Ready Workspace

Bienvenue dans l'atelier de travail sur [**Code Ready Workspace**](https://www.redhat.com/en/technologies/jboss-middleware/codeready-workspaces)


## Dévelloper dans le cloud.

[Code Ready Workspace](https://www.redhat.com/en/technologies/jboss-middleware/codeready-workspaces) est un solutions de développement collaborative native Kubernetes pour le développement rapide d'application. Il founit des environments de développement cohérents sur `Openshift` avec un IDE intégré au navigateur pour un développement rapide d'applications Natif à OpenShift, CodeReady workspace est construit sur le projet [Eclipse Che](https://www.eclipse.org/che/)et utilise Kubernetes et les conteneurs pour fournir aux membres de l'équipe de développement et/ou d'opération un environnement de développement cohérent, sécurisé qui requière aucune configuration. L'expérience est aussi rapide et familière qu'un environnement de développement intégré sur votre ordinateur portable. Disponible dans 
le Operator Hub de OpenShift, il fournit aux équipes une foundation plus rapide et fiable avec laquelle travailler, tout en donnant aux opérations un contrôle centralisé et une tranquillité d'esprit. 

### Caractéristiques principales

* `OpenShift-Natif:` Les développeur peuvent ce concentrer sur le code, sans avoir a comprendres les détails the Kubernetes et les administrateur eux peuvent gérer et monitorer les workspaces comme il le ferait pour de simple ressource kubernetes.

* `IDE dans un Navigateur:` CodeReady workspace comprend un IDE performant et familier qui fonctionne dans un nagigateur web et qui comprends le support pour Microsoft Visual Studio code et ses extensions. Les utilisateurs on seulement besoin d'avoir un ordinateur cabaple de rouler un navigateur pour pouvoir coder, tester et rouler leur code sur `OpenShift`.

* `Workspaces en 1 click`: Configuration de workspaces de façon centralisé, facilement partageable et cohérent. Fini avec la fameuse phrase "ça fonctionne sur ma machine". Les workspace comprennes:
    * Allocation de resourfes
    * Répertoire pour le code source
    * Runtime pour les applications
    * Outils pour "build"
    * Outlis de développement

* `Intégration de nouveau membre presque instantanné`: Tout le monde qui ont accès a un browser peut contribué au project en quelque minutes.

* `Large éventail d'options`: Les dévelopers peuvent profité du large éventail d'image de conteneur certifié pour développeur leurs applications.

* `Intégration d'entreprise`: Tout le dévelopment ainsi que l'accès au code source est fait de façon sécuritaire avec les mêmes outils que le rest de l'organisations.  CodeReay workspace comprend [Red Hat SSO](https://access.redhat.com/products/red-hat-single-sign-on) pour authentification et la sécurité.


## Aperçu

Dans cette atelier nous allons apprendre différent concepts en lien avec CodeReady workspace dans le but d'avoir un connaissance pratique de l'outils. L'atelier démontre certain concepts pour faciliter l'utilisation de CodeReady workspace.

### Sections:
 * [Prerequis](#prerequis)
 * [Installation de CodeReady Workspace](#installation)
 * [Connection d'un utilisateur](docs/user-connection.md)
 * [Installation du cli de Openshift](docs/cli-install.md)   
 * [Connecter à un GitHub Privé](docs/github-private.md)
 * [Création d'un workspace à partir de github](docs/workspace-creation.md)
 * [Utiliser CodeReady Workspace](docs/codeready-howto.md)

### Prerequis

 * Un cluster OpenShift pour installer CodeReady Container.
 * Un compte pour ce connecter au cluster
 * Du storage persistent sur le cluster

### Installation

Pour installer CodeReady workspace, il suivi d'installater Opérateur requis dans la console OpenShift. Suivre les [instruction suivante](docs/install-operator.md)faire l'installation de l'opérateur.