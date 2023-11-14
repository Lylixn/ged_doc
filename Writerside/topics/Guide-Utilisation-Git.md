# Guide Utilisation Git

## Status

* Voir le status du repository ce qui est modifié, ce qui est ajouté, ce qui est supprimé

```bash
git status
```

## Add

* Ajouter un fichier au prochain commit

```bash
git add <nom-du-fichier>
```

* Ajouter tous les fichiers au prochain commit

```bash
git add -A
```

## Commit

* Créer un commit avec un message

```bash
git commit -m "<message>"
```

* Créer un commit avec un message et ajouter tous les fichiers au prochain commit

```bash
git commit -am "<message>"
```

## Push

* Envoyer les commits sur le serveur

```bash
git push
```

## Pull

* Récupérer les commits du serveur

```bash
git pull
```

* Récupérer les commits du serveur et fusionner les branches

```bash
git pull --rebase
```

* Récupérer les commits de la branche develop du serveur et fusionner les branches

```bash
git pull origin develop
```

* Récupérer les commits du serveur et fusionner les branches en écrasant les commits locaux

```bash
git pull --rebase --autostash
```

* Récupérer les commits du serveur et fusionner les branches en écrasant les commits locaux et en écrasant les fichiers locaux

```bash
git pull --rebase --autostash --force
```

## Branch

* Créer une branche

```bash
git branch <nom-de-la-branche>
```

* Créer une branche et se placer dessus

```bash
git checkout -b <nom-de-la-branche>
```

* Se placer sur une branche

```bash
git checkout <nom-de-la-branche>
```

* Supprimer une branche

```bash
git branch -d <nom-de-la-branche>
```

* Supprimer une branche même si elle n'est pas fusionné

```bash
git branch -D <nom-de-la-branche>
```

* Renommer une branche

```bash
git branch -m <nom-de-la-branche> <nouveau-nom-de-la-branche>
```

* Renommer la branche actuelle

```bash
git branch -m <nouveau-nom-de-la-branche>
```

* Voir les branches

```bash
git branch
```

## Merge

* Fusionner une branche dans la branche actuelle

```bash
git merge <nom-de-la-branche>
```

* Fusionner une branche dans la branche actuelle en écrasant les commits locaux

```bash
git merge <nom-de-la-branche> --strategy-option theirs
```

* Fusionner une branche dans la branche actuelle en écrasant les commits locaux et en écrasant les fichiers locaux

```bash
git merge <nom-de-la-branche> --strategy-option theirs --strategy-option ours
```

## Log

* Voir les commits

```bash
git log
```

* Voir les commits avec les fichiers modifiés

```bash
git log --stat
```

* Voir les commits avec les fichiers modifiés et les lignes modifiés

```bash
git log --stat --patch
```

## Stash

* Cacher les modifications en cours

```bash
git stash
```

* Voir les modifications en cours

```bash
git stash list
```

* Récupérer les modifications en cours

```bash
git stash pop
```