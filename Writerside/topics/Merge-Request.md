# Merge Request

Avant de créer une MR, **le développeur s'assure que tous les changements dans les fichiers de
code ont été sauvegardés**. Le développeur vérifie les noms des fichiers dans lesquels des
changements ont été faits en vérifiant le statut de git sur le terminal avec la syntaxe suivante :

```bash
git status
```

Le développeur s'assure que la branche de destination est celle de **« develop »**

Pour effectuer une MR, voici le code **Bash** sur le terminal :

```bash
git add -A
git commit -m "GED-<numéro-de-ticket>: <message>"
git push origin <nom-de-la-branche>
```

Avant de confirmer la **MR** sur GitLab, le développeur vérifie les informations suivantes sur
**GitLab** :

![Merge Request](merge_request.png)

* **Le titre du MR** doit être correctement écrit
* **Faire un aperçu des changements faits** par rapport au ticket et **vérifier que tous les codes ont bien été poussés**.
* S’assurer que la **MR transite vers la bonne branche** de destination
* **N'oubliez pas d'ajouter un reviewer, un assigné et un label tag**

## Création d'un post sur Discord

Une fois la MR confirmée sur GitLab, le développeur va **créer un post Discord sur le salon de
discussion "MR"**. Le titre du post est le même que le **titre de la MR défini sur GitLab**. À la ligne
du post, **ajouter le lien GitLab et choisir le langage sur lequel le ticket a été implementé**.

**Ajouter les membres qui sont concernés par la MR** et faire le suivi de votre MR sur la discussion
du post créé.

L'exemple d'un post :

![Post Discord](discord_post.png)

## Suivi du Ticket sur JIRA

La prochaine étape consiste à **transiter le ticket de JIRA** qui a été envoyé pour une MR dans la
**colonne de Review** sur le tableau de bord de Jira

![jira](jira.png)

**Dans la description du ticket, venez rajouter votre procédure de test** dans le commentaire du
ticket et faites un suivi des notifications sur le ticket

## Gérer les conflits

Si le développeur a des conflits lors de la MR, il doit **résoudre les conflits** et **pousser les changements sur GitLab**.

**Vérifier que la branche “develop” est à jour** en effectuant une update sur l‘IDE de la branche
**“develop”**

Une fois la branche de **“develop”** mise à jour, **aller sur la branche du ticket sur laquelle il faut résoudre les conflits**

Sur le terminal **effectuer** :
```Bash
git Pull origin
```
Pour récupérer les fichiers de la branche
de “develop” **pour voir les conflits contre les fichiers de la branche** de votre ticket

Ensuite **sur l’IDE de PyCharm, gérer les conflits en allant dans l'onglet de GIT** (en bas à gauche
avec les deux branches)

*Note : Les conflits sont représentés lorsqu'il y a la présence de trois colonnes. Quand il y a
que deux colonnes présentent, il ne faut faire AUCUN changement sur les fichiers*