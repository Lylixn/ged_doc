# Connexion au terminal de la VM depuis Windows

- Vous pouvez maintenant vous connecter à votre VM via SSH
- Pour cela, il faut connaitre l'adresse IP ou le Nom de domaine de votre VM

<tabs>
    <tab title="Nom de domaine VM">
        <p>Ouvrez HyperV</p>
        <p>Le nom de la VM serra marquer ici :</p>
        <img src="nom_de_domaine.png" alt="nom de domaine" height="200"/>
    </tab>
    <tab title="Adresse ip">
        <ul>
            <li>Allez dans le terminal de votre VM</li>
            <li>Et executé la commande suivante</li>
            <li>
                <code-block lang="bash">ifconfig</code-block>
            </li>
            <li>Et bonne chance pour trouvé la bonne ip</li>
        </ul>
    </tab>
</tabs>

- Une fois que vous avez votre ip ouvrir un terminal sur votre machine Windows
- Vous devez aussi vous rappelez du nom d'utilisateur **que vous avez choisi lors de la création de la VM**
- Et executé la commande suivante

```bash
ssh <nom-utilisateur>@<ip ou nom de domaine>
```

- Vous allez devoir entré le mot de passe **de votre VM linux**
- Puis vous serrez connecté à votre VM en ssh depuis votre machine Windows

Chaque commande que vous executé dans le terminal de votre machine Windows serra executé dans le terminal de votre VM