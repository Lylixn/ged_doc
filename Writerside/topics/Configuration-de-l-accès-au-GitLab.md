# Configuration de l&apos;accès au GitLab

**Connecter vous en ssh au terminal de la VM**

## Génération de la clé SSH

```Bash
ssh-keygen
```

- Appuyer sur entrer pour valider le chemin par défaut
- Ecrivez un mot de passe pour votre clé SSH
- Ecrivez à nouveaux le mot de passe pour votre clé SSH

Votre clé à été généré dans le dossier **.ssh** de votre utilisateur (```/home/<nom-utilisateur>/.ssh```)

### Differente clé SSH

#### Clé Public

- La clé public est la clé que vous allez donner au serveur GitLab
- Elle se trouve dans le fichier **id_rsa.pub**
- Vous pouvez l&apos;afficher avec la commande suivante

```bash
cat ~/.ssh/id_rsa.pub
```

#### Clé Privé

- La clé privée est la clé que vous allez garder pour vous
- Elle se trouve dans le fichier **id_rsa**
- Vous pouvez l&apos;afficher avec la commande suivante

```bash
cat ~/.ssh/id_rsa
```

## Ajout de la clé SSH au GitLab

- Connectez vous à votre compte GitLab
- Cliquez sur votre avatar en haut à droite
- Cliquez sur **Settings**
- Cliquez sur **SSH Keys**
- Cliquez sur **Add new Key**
- Entré votre clé public dans le champs **Key**
- Le champs **Title** serra automatiquement remplis vous pouvez le changé si besoin
- Cliquez sur **Add Key**
- Vous pouvez maintenant vous connecter au GitLab avec la commande suivante

## Clonage du projet

- Aller sur le terminal de votre VM
- Mettez vous a l'emplacement où vous voulez stocker le projet
- Puis entrer la commande suivante

```bash
git clone git@gitlab.xefi.fr:xefi/GED/ged.git
```

- Entrer votre mot de passe de votre clé SSH
- Entré yes pour accepter la clé du serveur
- Le projet est maintenant cloné sur votre VM