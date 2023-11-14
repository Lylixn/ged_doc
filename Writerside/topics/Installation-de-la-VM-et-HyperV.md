# Installation de la VM et HyperV

## Installation de HyperV

- Cliquez sur rechercher
- Activer ou désactiver des fonctionnalités Windows
  ![Create new topic options](add_fonctionality.png){ width=290 }{border-effect=line}
- Cliquez dessus
- Cocher la case de HyperV et lancer l'installation

## Téléchargement de l'iso

<tabs>
    <tab title="Linux Mint (lourd)">
        <ul>
            <li>Aller sur <a href="https://www.linuxmint.com/edition.php?id=305">https://www.linuxmint.com/edition.php?id=305</a></li>
            <li>Descendez à Download Mirror</li>
            <li>Cliquez sur un mirror situé en France pour lancer le téléchargement</li>
        </ul>
    </tab>
    <tab title="Ubuntu Server (léger)">
        <ul>
            <li>Aller sur <a href="https://ubuntu.com/download/server">https://ubuntu.com/download/server</a></li>
            <li>Cliquez sur Download Ubuntu Server</li>
        </ul>
    </tab>
</tabs>



## Creation de la VM

- Sur le gestionnaire Hyper-V aller dans la section "Actions" à droite de l'écran et cliquer sur "Nouveau"
- Sélectionner "Ordinateur virtuel"
- Une nouvelle fenêtre "Assistant nouvel ordinateur virtuel" s'ouvre, dans la partie "Spécifier le nom et l'emplacement", préciser alors le nom de la VM (libre à l'utilisateur), vérifier que la case "Stocker l'ordinateur virtuel à un autre emplacement" est décochée et cliquer sur "Suivant"
- Dans la partie "Spécifier la génération", choisir "Génération 2" et cliquer sur "Suivant"
- Dans la partie "Affecter la mémoire", vérifier que la mémoire de démarrage est à 1024 Mo et que la case "Utiliser la mémoire dynamique pour cet ordinateur virtuel" est cochée et cliquer sur "Suivant"
- Dans la partie "Configurer la mise en réseau", cliquer sur le menu déroulant de "Connexion" et choisir "Default Switch" puis cliquer sur "Suivant"
- Dans la partie "Connecter un disque dur virtuel", vérifier que l'option "Créer un disque dur virtuel" est sélectionnée, ainsi que le nom est le même que celui spécifié précédemment et que la taille est de 127 Go et cliquer sur "Suivant"
- Dans la partie "Options d'installation", sélectionner l'option "Installer un système d'exploitation à partir d'un fichier image de démarrage" et cliquer sur "Parcourir..." puis sélectionner l'image téléchargée précédemment et cliquer sur "Suivant"
- La VM est prête, cliquer sur "Terminer"

## Lancement de la VM

- -Dans la partie "Ordinateurs virtuels", faire un clic droit sur la VM et sélectionner "Paramètres..." 
- aller dans la section "Sécurité" et dans la partie "Démarrage sécurisé"
- décocher la case "Activer le démarrage sécurisé" et cliquer sur "Ok"
![Create new topic options](secure_boot.png){ width=500 }{border-effect=line}
- Dans la section "Actions", cliquer sur "Démarrer" et vérifier que l'état de la VM est "Exécution" dans la partie "Ordinateurs virtuels"
![Create new topic options](virtual_computer.png){ width=500 }{border-effect=line}
- Dans la section "Actions", cliquer sur "Se connecter", une nouvelle fenêtre "Connexion à un ordinateur virtuel" s'ouvre
![Create new topic options](start_screen.png){ width=500 }{border-effect=line}
- Sélectionner l'image installée avec les flèches haut-bas du clavier (la première dans ce cas) et faire Entrée

## Installation de l'OS de la VM

<tabs>
    <tab title="Linux Mint">
        <ul>
            <li>Une fois le chargement fini vous serez sur le bureaux mint</li>
            <li>Double cliquez sur 'Install Linux Mint'</li>
            <li>Selectionnez 'Français' puis cliquez sur continuer</li>
            <li>Selectionner le Layout French avec le variant French</li>
            <li>Cliquer sur continuer et laissez les codecs multimedia decocher</li>
            <li>Selectioner Effacer le disque et installer Linux Mint puis cliquez sur 'Installez maintenant'</li>
            <li>Puis cliquez sur continuer</li>
            <li>Selectioner Paris puis Continuer</li>
            <li>Maintenant rentré vos informations :</li>
            <li>- nom d'utilisateur  <b>/!\ il serra utile plus tard pour ce connecté en SSH</b></li>
            <li>- mot de passe <b>/!\ il serra utile plus tard pour ce connecté en SSH</b></li>
            <li>Puis cliquez sur continuez</li>
            <li>l'installation se lancera ensuite</li>
            <li>Une fois terminé cliquez sur Redémarrer maintenant</li>
        </ul>
    </tab>
    <tab title="Ubuntu Server">
        <ul>
            <li>Une fois le chargement fini</li>
            <li><i>Dans Ubuntu Server il n'y a pas d'interface graphique vous devrez utiliser les flèches pour vous déplacez et entré ou espace pour selectionner ou cliquez</i></li>
            <li>Selectionner la langue Français et appuyer sur Entrée</li>
            <li>Si une mise à jour est proposez selectionner Mise à jour vers le nouveau programme</li>
            <li>Selectionner le Layout French avec le variant French</li>
            <li>Selectionner Ubuntu server et cocher "Search for third-party drivers"</li>
            <li>Pour la page <b>Network Connections, Proxy Adresse, Archive Mirror, Guided Storage Configuration cliquez directement sur done</b></li>
        </ul>
        <p>Une fois à Storage Configuration cliquez sur done puis continue</p>
        <ul>
            <li>Maintenant rentré vos informations :</li>
            <li>- name serra le nom d'affichage d'utilisateur</li>
            <li>- servers name serra le nom du pc</li>
            <li>- username serra le nom d'utilisateur <b>( /!\ il serra utile plus tard pour ce connecté en SSH)</b></li>
            <li>- password serra le mot de passe de votre session <b>( /!\ il serra utile plus tard pour ce connecté en SSH)</b></li>
        </ul>
        <ul>
            <li>Lorsqu'il proposera l'upgrade pour ubuntu pro selectionnez skip</li>
            <li>Vous selectionnerais ensuite isntall OpenSSH server</li>
            <li>Dans featured Server Snaps cliquez directement sur Done</li>
            <li>l'installation se lancera ensuite</li>
            <li>Une fois terminé cliquez sur Reboot Now</li>
        </ul>
    </tab>
</tabs>