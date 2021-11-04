# Configurer l'accès à GitHub

Il est possible de connecter CodeReady workspace vers des repos GitHub qui sont privés avec utilisation d'une [token personnel](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) sur GitHub.figuration est aussi nécessaire pour contribuer du code dans un repo public.

### Prerequis
* Être connecté à la console web de `OpenShift` avec son compte.
* Avoir un compte GitHub

## Création de la `token personnelle` sur GitHub.

1. À partir de votre compte [GitHub](github.com), sous votre profile, sélectionnez `setting`.

    ![GitHub setting](images/github-setting.png)

2. Sélectionné `Developer settings`

    ![GitHub dev](images/github-devsetting.png)

3. Sélectionné `Personal access tokens`

    ![GitHub personal token](images/github-personal-token.png)

7. Cliqué sur `Generate new token`et entrer les info.

![GitHub personal token 2](images/github-access-token.png)

* `Note`: Un nom pour la token
* `Expiration`: Choisir l'expiration requise pour respecter vos critères de sécurité. 
*  `Select scopes`: Doit sélectionné repo au minimum
* Cliqué `Generate token`

:warning: Copier la token qui vient d'être générée, car elle ne sera plus accessible.


## Créer les secrets dans OpenShift
:warning: cette étape peut-être fait qu'une fois que l'utilisateur s'est connecté a CodeReady workspace une première fois.

1. Se connecter à `OpenShift` avec le  `cli OpenShift`

2. Allez dans le projet qui contient le CodeReady workspace. Le nom du projet devrait ressemble à quelques chose du genre:  'username'-codeready
    ```
    oc project <your_project_name>
    ```

3. Créer le nouveau `Secret`. Pour ce faire nous devons utiliser la token fait dans github plus tôt, et remplacer les élément entre <, >
    ```
    oc create secret generic git-credentials-secret --from-literal=credentials=https://<GITHUB_USER>:<PERSONAL_TOKEN>@github.com
    ```

4. Une fois le secret créé, nous devons annoter le secret comme suit:
    ```
    oc annotate secret git-credentials-secret \
    che.eclipse.org/automount-workspace-secret='true' \
    che.eclipse.org/mount-path=/home/theia/.git-credentials \
    che.eclipse.org/mount-as=file \
    che.eclipse.org/git-credential='true'
    ```

5. Pour finir, créons un `label secret`
    ```
    oc label secret git-credentials-secret \
    app.kubernetes.io/part-of=che.eclipse.org \
    app.kubernetes.io/component=workspace-secret
    ```

:tada: FÉLICITATION

Vous vous êtes authentifié avec GitHub.

:point_right: Suivant: [Création d'un workspace à partir de GitHub](docs/workspace-creation.md)
