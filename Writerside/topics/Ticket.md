# Ticket

## Ticket attribué

Une fois qu'un ticket a été attribué
- le responsable du ticket recevra une notification sur la page
de notification de Jira. 
- Le responsable doit lire le ticket avec attention et :

1. **comprendre le type de ticket** et le message du ticket
2. **lire toutes les pièces jointes** associées au ticket
3. faire part de ses préoccupations par rapport à l'implémentation du ticket au Scrum Master.

![Ticket attribué](ticket_attribution.png)

## Mise en œuvre du ticket

Avant de commencer à travailler sur un ticket, le développeur doit :

### Mettre à jour son environnement local

- toujours mettre à jour la branche « develop » et extraire toutes les mises à jour sur son environnement local en faisant
un « pull » request sur la branche de « develop » comme suit sur l’image ci-dessous.

[Mettre à jour](Guide-Utilisation-Git.md#pull)

![Mettre à jour](pull.png)

### Nommer la branche

- Ensuite, le développeur doit **créer une nouvelle branche** à partir de « develop » ayant comme
  **nom de branche GED suivi du numéro de ticket**. *Par exemple, si le numéro de ticket est 123, le nom de la branche sera GED-123.*

- **Pour les cas d'exception** comme la mise à jour d'un environnement pour une démo, le
  développeur peut créer une nouvelle branche à partir d'une version d'un environnement
  stable. *(Par exemple : « v3.216.55-ged3 »)*

- Pour les cas d'exception où le développeur doit laisser le travail en cours sur un ticket et
  travailler sur un autre ticket plus prioritaire.

- Le développeur fait un « stash» sur Git sur la branche sur laquelle il travaille en cachant le
  travail en cours et créer la nouvelle branche avec le numéro de ticket prioritaire. Une fois le
  ticket prioritaire terminé, le développeur peut revenir au ticket de cache sur Git et continuer
  avec son répertoire de travail.

[Mettre en cache](Guide-Utilisation-Git.md#stash)

### Créer la branche

Pour créer une nouvelle branche, le développeur doit :

- Faire la commande suivante sur Git :

```bash
git checkout -b <nom-de-la-branche>
```

## Implémentation du ticket

Durant l’implémentation d’un ticket, le développeur travaille sur son ticket à partir de la
nouvelle branche créée.

Le développeur suit les meilleures pratiques du codage lors de l’implémentation d’un ticket et
s’en tenir à ce qui suit :

**À ne pas faire**
1. Des codes répétitifs
2. Des lignes noires non nécessaires
3. Avoir des logs inutiles à l'exception des logs de débogage
4. Faire des changements pour un ticket directement sur les fichiers de code sur GitLab

**Les meilleures pratiques du codage :**
1. Des codes **simples et concis** 
2. **Suivre les conventions** pour les classes, les méthodes, les fonctions et les variables 
3. **Indenter son code soigneusement** afin qu'il soit joliment représenté et facilement compréhensible 
4. **Effectuer des tests** de base avant de faire une MR 
5. **Transformer la sauvegarde quotidienne en un instinct**, valider la progression quotidienne des sous-fonctionnalités d'un ticket en poussant les codes nécessaires sur GitLab 
6. Ceux qui utilisent l'IDE « Pycharm », sélectionnent seulement les lignes de code significatives pour la sauvegarde sur GitLab 
7. Le message d'un commit contient toujours « GED- » suivi du numéro de ticket accompagné d'un message clair et précis qui décrit en quelques mots les changements apportés au ticket

## Merge Request

Avant de créer une MR, **le développeur s'assure que tous les changements dans les fichiers de
code ont été sauvegardés**. Le développeur vérifie les noms des fichiers dans lesquels des
changements ont été faits en vérifiant le statut de git sur le terminal avec la syntaxe suivante :

```bash
git status
```

Le développeur s'assure que la branche de destination est celle de « develop ».

Pour effectuer une MR, voici le code Bash sur le terminal :

```bash
git add -A
git commit -m "GED-<numéro-de-ticket>: <message>"
git push origin <nom-de-la-branche>
```

Avant de confirmer la MR sur GitLab, le développeur vérifie les informations suivantes sur
GitLab :

![Merge Request](merge_request.png)

* **Le titre du MR** doit être correctement écrit
* **Faire un aperçu des changements faits** par rapport au ticket et **vérifier que tous les codes ont bien été poussés**.
* S’assurer que la **MR transite vers la bonne branche** de destination
* **N'oubliez pas d'ajouter un reviewer, un assigné et un label tag**

### Creation d'un post sur Discord

Une fois la MR confirmée sur GitLab, le développeur va **créer un post Discord sur le salon de
discussion "MR"**. Le titre du post est le même que le **titre de la MR défini sur GitLab**. À la ligne
du post, **ajouter le lien GitLab et choisir le langage sur lequel le ticket a été implementé**.

**Ajouter les membres qui sont concernés par la MR** et faire le suivi de votre MR sur la discussion
du post créé.

L'exemple d'un post :

![Post Discord](discord_post.png)

### Suivi du Ticket sur JIRA

La prochaine étape consiste à **transiter le ticket de JIRA** qui a été envoyé pour une MR dans la
**colonne de Review** sur le tableau de bord de Jira.

![jira](jira.png)

**Dans la description du ticket, venez rajouter votre procédure de test** dans le commentaire du
ticket et faites une suivie des notifications sur le ticket.

### Gerer les conflits

Si le développeur a des conflits lors de la MR, il doit **résoudre les conflits** et **pousser les changements sur GitLab**.

**Vérifier que la branche “develop” est à jour** en effectuant une update sur l‘IDE de la branche
“develop”

Une fois la branche de “develop” mise à jour, **aller sur la branche du ticket sur laquelle il faut résoudre les conflits**

Sur le terminal effectuer un :
```Bash
git Pull origin
```
Pour récupérer les fichiers de la branche
de “develop” **pour voir les conflits contre les fichiers de la branche** de votre ticket

Ensuite **sur l’IDE de PyCharm, gérer les conflits en allant dans l'onglet de GIT** (en bas à gauche
avec les deux branches)

*Note : Les conflits sont représentés lorsqu'il y a la présence de trois colonnes. Quand il y a
que deux colonnes présentent, il ne faut faire AUCUN changement sur les fichiers*