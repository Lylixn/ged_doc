# Ticket

## Ticket attribué

Une fois qu'un ticket a été attribué
- le responsable du ticket recevra une notification sur la page
de notification de Jira. 
- Le responsable doit lire le ticket avec attention et :

1. **comprendre le type de ticket** et le message du ticket
2. **lire toutes les pièces jointes** associées au ticket
3. faire part de ses préoccupations par rapport à l'implémentation du ticket au Scrum Master.

![Ticket attribué](ticket_attribution.png)

## Mise en œuvre du ticket

Avant de commencer à travailler sur un ticket, le développeur doit :

- toujours mettre à jour la branche « develop » et extraire toutes les mises à jour sur son environnement local en faisant
un « pull » request sur la branche de « develop » comme suit sur l’image ci-dessous.

[Mettre à jour](Guide-Utilisation-Git.md#pull)

![Mettre à jour](pull.png)

- Ensuite, le développeur doit **créer une nouvelle branche** à partir de « develop » ayant comme
  **nom de branche GED suivi du numéro de ticket**. *Par exemple, si le numéro de ticket est 123, le nom de la branche sera GED-123.*
- Pour les cas d'exception comme la mise à jour d'un environnement pour une démo, le
  développeur peut créer une nouvelle branche à partir d'une version d'un environnement
  stable. *(Par exemple : « v3.216.55-ged3 »)*