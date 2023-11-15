# Configuration du SSH

- Vous devez avoir <b>terminé l'installation</b> et être <b>connecté</b> à la <b>session</b> de votre <b>VM</b>

## Linux Mint

- Allez dans le <b>terminal</b> de votre VM
- Exécutez <b>chaque commande dans l'ordre</b>

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
- Si vous avez suivi la <b>partie précedente</b> vous avez deja installé le <b>SSH</b>

#### Vous pouvez maintenant fermer la fenetre de la VM et fermer Hyper-V, votre VM continuera à fonctionner en arrière-plan