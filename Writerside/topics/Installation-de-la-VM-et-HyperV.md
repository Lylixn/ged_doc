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

- créé la vm
- lancer vm

## Installation de l'OS de la VM

<tabs>
    <tab title="Linux Mint">
        <ul>
            <li>Lorsqu'il y a marquer 'Start Linux Mint 21.2 Cinnamon 64-bit" Appuyer sur entré</li>
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
            <li>Une fois terminé cliquez sur Reboot Now</li>
        </ul>
    </tab>
    <tab title="Ubuntu Server">
        <ul>
            <li>Lorsqu'il y a marquer 'Try or Install ubuntu Server' Appuyer sur entré</li>
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