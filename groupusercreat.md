# Créer les comptes utilisateurs du domaine


1. Depuis le Gestionnaire de serveur, cliquer sur le menu Outils et choisir Utilisateurs et ordinateurs Active Directory (tout en bas).
![1](https://github.com/user-attachments/assets/4964791d-9c3a-4a8b-a3c1-0e8f76fe3ddc)


2. Dérouler « domaine.local » et Users pour voir la liste des utilisateurs et des groupes qui existent déjà, par défaut dans Windows Server 2022. On notera que figure déjà le compte « Administrateur » que l’on utilise déjà.


3. Faire un clic droit sur le nom du domaine, Nouveau, Unité d’organisation.![3](https://github.com/user-attachments/assets/bad7c644-3ba1-4142-be02-7564ec2444ac)

4. Donner un nom à cette UO / OU, par exemple le nom de l’entreprise.![4](https://github.com/user-attachments/assets/71f73472-8509-425c-bb7c-148d4c87d318)

5. Ce nouveau « dossier » s’ajoute au même niveau que Users.

6. Faire un clic droit sur la nouvelle UO (Wilders_students), Nouveau, group.
Renseigner nom ![5 creation de groupe](https://github.com/user-attachments/assets/4460d500-acbb-4a91-905a-8fb0d4319649)

7. Faire un clic droit sur la nouvelle UO (Wilders_students), Nouveau, User. Prénom, Nom, Nom d’ouverture de session (login) :![6](https://github.com/user-attachments/assets/7b8b1ffe-2193-4d67-8039-f6792ba2c5c4)
![6B](https://github.com/user-attachments/assets/3262893c-84c1-42a4-abe4-f7bb7611fe39)
![6C](https://github.com/user-attachments/assets/1b25d48e-d3e4-4425-9aac-16b354c53c68)

8. Faire un clic droit sur le nouvel utilisateur et Add to group![6D](https://github.com/user-attachments/assets/50130c72-0bb5-45ae-8add-e025a122b459)

9. Ecrire le nom du groupe (Wilders_students) et faire Check Names puis OK ![6E](https://github.com/user-attachments/assets/d67b4695-ce65-4c12-829c-1db8d7253ef3)
![resultat](https://github.com/user-attachments/assets/0d47fb6f-7b24-4c19-81d7-9c70b494854c)



Bravo !!
