# Installer Active Directory sur Windows Server 2022


1. Première étape, a priori déjà réglée : ouvrir une session en Administrateur local ou avec un compte qui fait partie des administrateurs locaux du serveur.

2. Dans le Gestionnaire de serveur, cliquer sur l’étape « 2 – Ajouter des rôles et des fonctionnalités » .

3. Choisir « Installation basée sur un rôle ou une fonctionnalité » .
C![addroles](https://github.com/user-attachments/assets/6e80f9d1-b8c0-4bac-b96c-bc96c2ec7fa9)

4. Choisir la bonne machine dans le pool de serveurs
![serveur](https://github.com/user-attachments/assets/073604bc-b13d-48ee-b04b-687e4414a95d)


5. Cocher le rôle « Services AD DS » pour Active Directory Domain Services. Remarque : les rôles DNS et DHCP seront ajoutés plus tard.
6. ![ad](https://github.com/user-attachments/assets/20a5aa92-af70-4ee5-9fe9-e668445d0a32)

7. Valider aussi l’ajout de rôles et de fonctionnalités complémentaires, requises pour l’installation de ADDS.
![ad2](https://github.com/user-attachments/assets/51ecff79-568d-41cd-8428-968e335e0573)

8. L’écran suivant permet d’ajouter des fonctionnalités, ne rien faire et cliquer sur Suivant.

9. Vérifier le résumé de l’installation et cliquer sur « Installer » pour démarrer l’opération.

10. En laissant l’écran ouvert, à la fin du processus, on peut lire « Configuration requise. Installation réussie sur SERVEUR » et surtout la ligne « Promouvoir ce serveur en contrôleur de domaine » : c’est sur cette phrase qu’il faut cliquer pour convertir le serveur en contrôleur de domaine du réseau.

![promouvoir](https://github.com/user-attachments/assets/631e8363-77ba-446b-aa70-3dd60017a756)

11. Dans notre configuration exemple, il s’agit du premier serveur d’un nouveau réseau. Choisir « Ajouter une nouvelle forêt » pour configurer un domaine neuf. Indiquer un Nom de domaine racine, par exemple domaine.local ou entreprise.local.

![ajout foret](https://github.com/user-attachments/assets/d17a8aa0-546a-4120-b7af-a3175b87e26a)


12. Laisser coché l’ajout de la fonctionnalité Serveur DNS pour ajouter ce rôle et indiquer un mot de passe de récupération des services d’annuaire (DSRM). Ce mot de passe ne doit absolument pas être perdu.

![mdp](https://github.com/user-attachments/assets/cd72b73c-1239-483f-b268-f6dac4d3fa17)


13. Un message d’erreur en jaune vient alerter de la délégation du serveur DNS. Il n’y a rien à faire à ce stade, cliquer simplement sur Suivant pour continuer.

![erreur](https://github.com/user-attachments/assets/9637559b-e77b-410c-8bad-c2f7350cd9c6)


14. Nous avons précédemment choisi un nom de domaine complet (FQDN), il faut maintenant indiquer l’équivalent NetBIOS pour les anciens appareils qui ne gèrent pas les noms de domaines qualifiés. Par exemple, pour « domaine.local » on pourra choisir le NetBIOS « DOMAINE » .

![netbios](https://github.com/user-attachments/assets/1d37d5e5-ad40-483d-9878-a3021b47416f)


15. Valider l’emplacement de la base de données AD DS, des journaux d’historique et pour SYSVOL. Laisser les dossiers proposés par défaut (NTDS et SYSVOL dans C:\Windows).

16. Un récapitulatif résume la configuration qui va être appliquée. Cliquer sur Suivant pour continuer.

17. Une dernière vérification est effectuée, des notifications sont affichées mais cliquer sur Installer pour démarrer le processus.

![verifi](https://github.com/user-attachments/assets/e9d7dead-f818-4411-93ca-7e527e99d52f)


18. L’opération dure quelques minutes et le redémarrage de Windows prendra plus de temps que d’habitude, le temps de configurer le contrôleur de domaine.

19. La connexion à Windows doit maintenant se faire sur le domaine pour utiliser le compte Administrateur du domaine. Utiliser le mot de passe du compte Administrateur créé lors de l’installation de Windows Server 2016.



