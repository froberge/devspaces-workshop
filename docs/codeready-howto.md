# Utilisation de CodeReady Workspace.

CodeReady Workspace est une solution de développement collaboratif native Kubernetes pour le développement rapide d'application qui fonctionne sur OpenShift.

![Welcome screen](images/crw-create-workspace.png)

Caractéristiques:
* [Workspaces](#workspace)
* [IDE](#ide)


## Workspace

Un workspace représente l'endroit ou le projet vie. Selon les paramètres mis en place par l'administrateur du cluster chaque utilisateur pourra avoir 1+ workspace qui roule simultanément.

Il existe plusieurs façons de créer un workspace.

1. Importer a partir d'un repo Git
![Git import](images/custom-devfile.png)
2. Sélectionné à partir d'un gabarit existant

3. Créer un `Custom Workspace` en générant un Devfile
![Custom workspace](images/github-repo-url.png)

4. À partir d'une application qui est déjà dans OpenShift
![OpenShift workspace](images/ocp-codeready-app.png)


## IDE

IDE ressemble étrangement à VSCode et nous donnes les mêmes fonctionnalités.
* Connexion à GitHub avec un onglet dédié
* Remote debugging
* Accès à un terminal.


:point_right: Retour: [Table des matières](../README.md#table-des-matières)

