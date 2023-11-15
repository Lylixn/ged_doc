# Installation de la VM et Hyper-V

## Installation de Hyper-V

- Cliquez sur <b>Rechercher</b>
- Sélectionnez <b>Activer ou désactiver des fonctionnalités Windows</b>
  ![Create new topic options](add_fonctionality.png){ width=290 }{border-effect=line}
- Cochez la case de <b>Hyper-V</b> et lancez l'installation

## Téléchargement de l'image

<tabs>
    <tab title="Linux Mint (lourd)">
        <ul>
            <li>Allez sur <a href="https://www.linuxmint.com/edition.php?id=305"><b>https://www.linuxmint.com/edition.php?id=305</b></a></li>
            <li>Descendez à <b>Download Mirror</b></li>
            <li>Cliquez sur un mirror situé en <b>France</b> pour <b>lancer le téléchargement</b></li>
        </ul>
    </tab>
    <tab title="Ubuntu Server (léger)">
        <ul>
            <li>Aller sur <a href="https://ubuntu.com/download/server"><b>https://ubuntu.com/download/server</b></a></li>
            <li>Cliquez sur <b>Download Ubuntu Server</b></li>
        </ul>
    </tab>
</tabs>



## Création de la VM

- Sur le gestionnaire <b>Hyper-V</b>, allez dans la section <b>Actions</b> à droite de l'écran et cliquez sur <b>Nouveau</b>
- Sélectionnez <b>Ordinateur virtuel</b>
- Une nouvelle fenêtre <b>Assistant nouvel ordinateur virtuel</b> s'ouvre, dans la partie <b>Spécifier le nom et l'emplacement</b>, précisez alors le <b>nom</b> de la VM (libre à l'utilisateur), vérifiez que la case <b>Stocker l'ordinateur virtuel à un autre emplacement</b> est décochée et cliquez sur <b>Suivant</b>
- Dans la partie <b>Spécifier la génération</b>, choisissez <b>Génération 2</b> et cliquez sur <b>Suivant</b>
- Dans la partie <b>Affecter la mémoire</b>, vérifiez que la mémoire de démarrage est à <b>1024 Mo</b> et que la case <b>Utiliser la mémoire dynamique pour cet ordinateur virtuel</b> est cochée et cliquez sur <b>Suivant</b>
- Dans la partie <b>Configurer la mise en réseau</b>, cliquez sur le menu déroulant de <b>Connexion</b> et choisissez <b>Default Switch</b> puis cliquez sur <b>Suivant</b>
- Dans la partie <b>Connecter un disque dur virtuel</b>, vérifiez que l'option <b>Créer un disque dur virtuel</b> est sélectionnée, ainsi que le <b>nom</b> est le même que celui spécifié précédemment et que la taille est de <b>127 Go</b> et cliquez sur <b>Suivant</b>
- Dans la partie <b>Options d'installation</b>, sélectionnez l'option <b>Installer un système d'exploitation à partir d'un fichier image de démarrage</b> et cliquez sur <b>Parcourir...</b> puis sélectionnez <b>l'image</b> téléchargée précédemment et cliquez sur <b>Suivant</b>
- La <b>VM</b> est prête, cliquez sur <b>Terminer</b>

## Lancement de la VM

- Dans la partie <b>Ordinateurs virtuels</b>, faites un clic droit sur la VM et sélectionner <b>Paramètres...</b>
- Allez dans la section <b>Sécurité</b> et dans la partie <b>Démarrage sécurisé</b> décochez la case <b>Activer le démarrage sécurisé</b> et cliquez sur <b>Ok</b>
![Create new topic options](secure_boot.png){ width=500 }{border-effect=line}
- Dans la section <b>Actions</b>, cliquez sur <b>Démarrer</b> et vérifiez que l'état de la VM est <b>Exécution</b> dans la partie <b>Ordinateurs virtuels</b>
![Create new topic options](virtual_computer.png){ width=500 }{border-effect=line}
- Dans la section <b>Actions</b>, cliquez sur <b>Se connecter</b>, une nouvelle fenêtre <b>Connexion à un ordinateur virtuel</b> s'ouvre
![Create new topic options](start_screen.png){ width=500 }{border-effect=line}
- Sélectionnez <b>l'image</b> installée avec les flèches haut-bas du clavier (la première dans ce cas) et faites <b>Entrée</b>

## Installation de l'OS de la VM

<tabs>
    <tab title="Linux Mint">
        <ul>
            <li>Une fois le <b>chargement terminé</b> vous serez sur le bureau <b>Mint</b></li>
            <li>Double-cliquez sur <b>Install Linux Mint</b></li>
            <li>Selectionnez <b>Français</b> puis cliquez sur <b>Continuer</b></li>
            <li>Selectionnez le Layout <b>French</b> avec le variant <b>French</b></li>
            <li>Cliquer sur <b>Continuer</b> et laissez les <b>codecs multimedia</b> decochés</li>
            <li>Sélectionner <b>Effacer le disque et installer Linux Mint</b> puis cliquez sur <b>Installez maintenant</b></li>
            <li>Puis cliquez sur <b>Continuer</b></li>
            <li>Sélectionner <b>Paris</b> puis <b>Continuer</b></li>
            <li>Rentrez vos <b>informations</b> :</li>
            <li>- nom d'utilisateur <b>/!\ il sera utile plus tard pour se connecter en SSH</b></li>
            <li>- mot de passe <b>/!\ il sera utile plus tard pour se connecter en SSH</b></li>
            <li>Puis cliquez sur <b>Continuer</b></li>
            <li><b>L'installation</b> se lancera ensuite</li>
            <li>Une fois terminé cliquez sur <b>Redémarrer maintenant</b></li>
        </ul>
    </tab>
    <tab title="Ubuntu Server">
        <ul>
            <li>Une fois le <b>chargement terminé</b></li>
            <li><i>Dans <b>Ubuntu Server</b> il n'y a pas d'interface graphique, vous devrez utiliser les <b>flèches</b> pour vous déplacer et <b>Entrée</b> ou <b>Espace</b> pour sélectionner ou cliquer</i></li>
            <li>Sélectionnez la langue <b>Français</b> et appuyer sur <b>Entrée</b></li>
            <li>Si une mise à jour est proposée sélectionnez <b>Mise à jour vers le nouveau programme</b></li>
            <li>Sélectionnez le Layout <b>French</b> avec le variant <b>French</b></li>
            <li>Sélectionnez <b>Ubuntu Server</b> et cochez <b>Search for third-party drivers</b></li>
            <li>Pour la page <b>Network Connections, Proxy Adresse, Archive Mirror, Guided Storage Configuration</b> cliquez directement sur <b>Done</b></li>
        </ul>
        <p>Une fois à <b>Storage Configuration</b> cliquez sur <b>Done</b> puis <b>Continue</b></p>
        <ul>
            <li>Rentrez vos <b>informations</b> :</li>
            <li>- <b>name</b> sera le nom d'affichage d'utilisateur</li>
            <li>- <b>servers name</b> sera le nom du PC</li>
            <li>- <b>username</b> sera le nom d'utilisateur <b>( /!\ il sera utile plus tard pour se connecter en SSH)</b></li>
            <li>- <b>password</b> sera le mot de passe de votre session <b>( /!\ il sera utile plus tard pour se connecter en SSH)</b></li>
        </ul>
        <ul>
            <li>Lorsqu'il proposera l'upgrade pour <b>Ubuntu Pro</b> sélectionnez <b>Skip</b></li>
            <li>Sélectionnez <b>Install OpenSSH Server</b></li>
            <li>Dans <b>Featured Server Snaps</b> cliquez directement sur <b>Done</b></li>
            <li><b>L'installation</b> se lancera ensuite</li>
            <li>Une fois <b>terminé</b> cliquez sur <b>Reboot Now</b></li>
        </ul>
    </tab>
</tabs>