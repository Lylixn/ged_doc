# Connexion au terminal de la VM depuis Windows

- Vous pouvez maintenant vous <b>connecter à votre VM via SSH</b>
- Pour cela, il faut connaître <b>l'adresse IP</b> ou le <b>Nom de domaine</b> de votre <b>VM</b>

<tabs>
    <tab title="Nom de domaine VM">
        <p>Ouvrez <b>Hyper-V</b></p>
        <p>Le <b>nom</b> de la VM sera marqué ici :</p>
        <img src="nom_de_domaine.png" alt="nom de domaine" height="200"/>
    </tab>
    <tab title="Adresse IP">
        <ul>
            <li>Allez dans le <b>terminal</b> de votre VM</li>
            <li>Exécutez la <b>commande suivante</b>:</li>
            <li>
                <code-block lang="bash">ifconfig</code-block>
            </li>
            <li><b>L'IP</b> est normalement celle de la carte réseau <b>enp0s3</b></li>
        </ul>
    </tab>
</tabs>

- Une fois que vous avez votre <b>IP</b> ouvrez un terminal sur votre machine <b>Windows</b>
- Vous devez aussi vous rappeler du <b>nom d'utilisateur</b> **que vous avez choisi lors de la création de la VM**
- Executez la <b>commande suivante</b>:

```bash
ssh <nom-utilisateur>@<ip ou nom de domaine>
```

- Vous allez devoir entrer le <b>mot de passe</b> **de votre <b>VM Linux</b>**
- Puis vous serez connecté à votre VM en <b>SSH</b> depuis votre machine <b>Windows</b>

Chaque <b>commande</b> que vous exécutez dans le <b>terminal de votre machine Windows</b> sera exécutée dans le <b>terminal de votre VM</b>