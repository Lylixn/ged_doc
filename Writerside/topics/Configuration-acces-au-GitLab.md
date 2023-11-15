# Configuration de l&apos;accès au GitLab

**Connectez-vous en SSH au terminal de la VM**

## Génération de la clé SSH

```Bash
ssh-keygen
```

- Appuyez sur <b>Entrée</b> pour valider le chemin par défaut
- Ecrivez un <b>mot de passe</b> pour votre clé SSH
- Ecrivez à nouveau le <b>mot de passe</b> pour votre clé SSH

<b>Votre clé à été générée</b> dans le dossier **.ssh** de votre utilisateur (/home/nom-utilisateur/.ssh)

### Différents types de clé SSH

#### Clé Publique

- La <b>clé publique</b> est la clé que vous allez donner au <b>serveur GitLab</b>
- Elle se trouve dans le fichier **id_rsa.pub**
- Vous pouvez l&apos;afficher avec la <b>commande suivante</b>:

```bash
cat ~/.ssh/id_rsa.pub
```

#### Clé Privée

- La <b>clé privée</b> est la clé que vous allez garder pour vous
- Elle se trouve dans le fichier **id_rsa**
- Vous pouvez l&apos;afficher avec la <b>commande suivante</b>:

```bash
cat ~/.ssh/id_rsa
```

## Ajout de la clé SSH au GitLab

- <b>Connectez-vous</b> à votre compte <b>GitLab</b>
- Cliquez sur votre <b>avatar</b> en haut à droite
- Cliquez sur **Preferences**
- Cliquez sur **SSH Keys**
- Cliquez sur **Add new Key**
- Entrez votre clé publique dans le champ **Key**
- Le champ **Title** sera automatiquement rempli, vous pouvez le changer si besoin
- Cliquez sur **Add Key**

## Clonage du projet

- Allez sur le <b>terminal de votre VM</b>
- Mettez-vous à <b>l'emplacement</b> où vous voulez <b>stocker le projet</b>
- Entrez la <b>commande suivante</b>:

```bash
git clone git@gitlab.xefi.fr:xefi/GED/ged.git
```

- Entrez votre <b>mot de passe</b> de votre clé SSH
- Entrez <b>yes</b> pour accepter la <b>clé du serveur</b>
- Le <b>projet</b> est maintenant <b>cloné sur votre VM</b>