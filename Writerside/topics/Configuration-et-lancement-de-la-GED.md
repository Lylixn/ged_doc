# Configuration et lancement de la GED

## Configuration de la GED

### Configuration de docker

- copier-coller le fichier `docker-compose.local.yml` et renommer le `docker-compose.yml`
- dans le fichier `docker-compose.yml` supprimer ces differentes partie :

<table>
    <tr>
        <td>Partie à supprimer</td>
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

- mettez-vous à la racine du projet
- lancer les commandes suivantes :

```Bash
cd project/webapp && npm install
```
*car personne n'a merge mon nouveau dockerfile*

## Lancement de la GED

- lancer la commande `docker compose up -d` pour lancer la GED
- Puis lancer la commande `docker compose restart api-eddy` *car personne n'a merge mon nouveau dockerfile*