# Créer une instance de OpenShift Dev Spaces.

Maintenant que l'opérateur est installé, nous devons créer une instance de CodeReady Workspace dans le cluster.

## Étapes:

1. Dans le tab `Operator -> Installed Operators`
![Installed Operator Tab](images/installed-operators.png)


2. Cliqué sur l’opérateur Red Hat OpenShift Dev Spaces pour l'ouvrir:
![CRW install](images/crw-install-operator.png)


3. Dans la section `Details`, sous `OpenShift Dev Spaces instance Specification` cliquer sur `Create instance`.
![Create Workspace](images/crw-cluster-creation.png)

    Dans la section storage changeons la strategie de storage pour `per-workspace`.
    ![Create Workspace Storage](images/crw-cluster-creation-storage.png)

    Cliqué sur `Create`


4. OpenShift commencera la création du `CheCluster`.  
    ![Create Recaps](images/crw-cluster-recap.png)

    Cliqué sur le cluster qui vient d'être créé pour voir les détails.
    ![Cluster details](images/crw-cluster-detail.png)

    `OpenShift Dev Spaces` est prêt, lorsque le `OpenShift Dev Spaces URL` apparait.

:tada: FÉLICITATION

Vous avez construit l'instance du OpenShift Dev Spaces requis pour son utilisation. Vous pouvez maintenant partager l’URL avec les développeurs. Leur environnement sera créé lors de leur première connexion.

:point_right: Suivant: [Connection d'un utilisateur](user-connection.md)
