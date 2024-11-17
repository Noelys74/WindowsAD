# Créer les comptes utilisateurs du domaine


1. Depuis le Gestionnaire de serveur, cliquer sur le menu Outils et choisir Utilisateurs et ordinateurs Active Directory (tout en bas).


2. Dérouler « domaine.local » et Users pour voir la liste des utilisateurs et des groupes qui existent déjà, par défaut dans Windows Server 2016. On notera que figure déjà le compte « Administrateur » que l’on utilise déjà.

3. Pour mieux s’en sortir et ne pas se mélanger avec les comptes intégrés, nous allons créer un dossier pour les utilisateurs de notre société (Unité d’Organisation, OU en anglais). Ce « super groupe » sera plus facile à gérer, par exemple avec des GPO.

Faire un clic droit sur le nom du domaine, Nouveau, Unité d’organisation.

tutoriel Windows Server 2016 WS2016 Active Directory users utilisateurs OU

4. Donner un nom à cette UO / OU, par exemple le nom de l’entreprise.

tutoriel Windows Server 2016 WS2016 Active Directory users utilisateurs OU

5. Ce nouveau « dossier » s’ajoute au même niveau que Users.

6. Faire un clic droit sur la nouvelle UO (Wilders_students), Nouveau, group.

Renseigner nom
7. Faire un clic droit sur la nouvelle UO (Wilders_students), Nouveau, User.

Prénom, Nom, Nom d’ouverture de session (login) :

8. Faire un clic droit sur le nouvel utilisateur et Add to group

9. Ecrire le nom du groupe (Wilders_students) et faire Check Names puis OK 


Bravo !!
