# Introduction à Red Hat CodeReady Workspace

Bienvenue dans l'atelier de travail sur [**Code Ready Workspace**](https://www.redhat.com/en/technologies/jboss-middleware/codeready-workspaces)


## Développé dans le cloud.
[CodeReady Workspace](https://www.redhat.com/en/technologies/jboss-middleware/codeready-workspaces) est une solution de développement collaboratif native Kubernetes pour le développement rapide d'application. Il fournit des environnements de développement cohérent sur OpenShift avec un IDE intégré au navigateur pour un développement rapide d'applications natif à OpenShift, CodeReady workspace est construit sur le projet [Eclipse Che](https://www.eclipse.org/che/) et utilise Kubernetes et les conteneurs pour fournir aux membres de l'équipe de développement et/ou d'opération un environnement de développement cohérent, sécurisé qui ne demande aucune configuration. L'expérience est aussi rapide et familière qu'un environnement de développement intégré sur votre ordinateur portable. Disponible dans le Operator Hub d’OpenShift, il fournit aux équipes une fondation plus rapide et fiable avec laquelle travailler, tout en donnant aux opérations un contrôle centralisé et une tranquillité d'esprit. 

### Caractéristiques principales

* `OpenShift-Natif:` les développeurs peuvent se concentrer sur le code, sans avoir à comprendre les détails de Kubernetes et les administrateurs eux peuvent gérer et surveiller les workspaces comme il le ferait pour de simples ressources Kubernetes.

* `IDE dans un navigateur:` CodeReady workspace comprend un IDE performant et familier qui fonctionne dans un navigateur web et qui comprends le support pour Microsoft Visual Studio code et ses extensions. Les utilisateurs ont seulement besoin d'avoir un ordinateur capable de rouler un navigateur pour pouvoir coder, tester et rouler leur code sur `OpenShift`.

* `Workspaces en 1 clic`: Configuration de workspaces de façon centralisé, facilement partageable et cohérent. Fini avec la fameuse phrase "ça fonctionne sur ma machine". Les workspaces comprennent:
* Allocation de ressources
* Répertoire pour le code source
* Runtime pour les applications
* Outils pour "build"
* Outils de développement

* `Intégration de nouveau membre presque instantanée`: Tout le monde qui ont accès à un navigateur peut contribuer au projet en quelques minutes.

* `Large éventail d'options`: Les développeurs peuvent profiter d’un large éventail d'images de conteneur certifié pour développer leurs applications.

* `Intégration d'entreprise`: Tout le développement ainsi que l'accès au code source sont faits de façon sécuritaire avec les mêmes outils que le reste de l'organisation.  CodeReady workspace comprend [Red Hat SSO](https://access.redhat.com/products/red-hat-single-sign-on) pour l’authentification et la sécurité.

## Aperçu

Dans cet atelier, nous allons apprendre différents concepts en lien avec CodeReady workspace dans le but d'avoir une connaissance pratique de l'outil. L'atelier démontre certains concepts pour faciliter l'utilisation de CodeReady workspace.

### Table des matières
 * [Prerequis](#prerequis)
 * [Installation de CodeReady Workspace](#installation)
 * [Connexion d'un utilisateur](docs/user-connection.md)
 * [Installation du cli d’OpenShift](docs/cli-install.md)   
 * [Authentication à GitHub](docs/github-private.md)
 * [Création d'un workspace à partir de GitHub](docs/workspace-creation.md)
 * [Utiliser CodeReady Workspace](docs/codeready-howto.md)

### Prérequis

 * Un cluster OpenShift pour installer CodeReady Container.
 * Un compte pour se connecter au cluster
 * De l’entreposage persiste sur le cluster

### Installation

Pour installer CodeReady workspace, il suivit d'installer l’opérateur requis dans la console d’OpenShift. Suivre les [instruction suivante](docs/install-operator.md) pour faire l'installation de l'opérateur.