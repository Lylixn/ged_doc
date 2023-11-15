# Configuration et lancement de la GED

## Configuration de la GED

### Configuration de Docker

- <b>Copier-collez</b> le fichier `docker-compose.local.yml` et <b>renommez</b> le `docker-compose.yml`
- Dans le fichier `docker-compose.yml` <b>supprimez</b> ces differentes parties :

<table>
    <tr>
        <td><b>Partie à supprimer</b></td>
    </tr>
    <tr>
        <td>api-taxged</td>
    </tr>
    <tr>
        <td>workers-taxged</td>
    </tr>
    <tr>
        <td>api-psabe</td>
    </tr>
    <tr>
        <td>workers-psabe</td>
    </tr>
    <tr>
        <td>api-automobile</td>
    </tr>
    <tr>
        <td>workers-automobile</td>
    </tr>
    <tr>
        <td>mssql-taxged</td>
    </tr>
    <tr>
        <td>mssql-psabe</td>
    </tr>
    <tr>
        <td>mssql-automobile</td>
    </tr>
</table>

### Installation des dépendances

- Mettez-vous à la <b>racine du projet</b>
- Lancez les <b>commandes suivantes</b> :

```Bash
cd project/webapp && npm install
```
*car personne n'a merge mon nouveau Dockerfile*

## Lancement de la GED

- Lancez la <b>commande</b> `docker compose up -d` pour lancer la GED
- Puis lancez la <b>commande</b> `docker compose restart api-eddy` *car personne n'a merge mon nouveau Dockerfile*