# Configuration du SSH

- Vous devez avoir terminé l'installation et être connecter a la session votre VM

## Linux Mint

- Aller dans le terminal de votre VM
- Et executé chaque commande dans l'ordre

```Bash
sudo apt-get update && sudo apt-get upgrade -y
```

```Bash
sudo apt-get install openssh-server -y
```

```Bash
sudo systemctl enable ssh --now && sudo systemctl start ssh
```

## Ubuntu Server
- Si vous avez suivis la partie précedente vous avez deja installé le SSH

#### Vous pouvez maintenant fermer la fenetre de la VM et fermer hyperV, votre VM continuera a fonctionner en background