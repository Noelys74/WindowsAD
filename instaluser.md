# Installer Active Directory sur Windows Server 2022


1. Première étape, a priori déjà réglée : ouvrir une session en Administrateur local ou avec un compte qui fait partie des administrateurs locaux du serveur.

2. Dans le Gestionnaire de serveur, cliquer sur l’étape « 2 – Ajouter des rôles et des fonctionnalités » .

3. Choisir « Installation basée sur un rôle ou une fonctionnalité » .
Capture 


4. Dans notre exemple, le serveur est le seul du réseau, sinon choisir la bonne machine dans le pool de serveurs.
Capture

5. Cocher le rôle « Services AD DS » pour Active Directory Domain Services. Remarque : les rôles DNS et DHCP seront ajoutés plus tard.
Capture

6. Valider aussi l’ajout de rôles et de fonctionnalités complémentaires, requises pour l’installation de ADDS.
CApture

7. L’écran suivant permet d’ajouter des fonctionnalités, ne rien faire et cliquer sur Suivant.

8. Vérifier le résumé de l’installation et cliquer sur « Installer » pour démarrer l’opération.

9. En laissant l’écran ouvert, à la fin du processus, on peut lire « Configuration requise. Installation réussie sur SERVEUR » et surtout la ligne « Promouvoir ce serveur en contrôleur de domaine » : c’est sur cette phrase qu’il faut cliquer pour convertir le serveur en contrôleur de domaine du réseau.

Capture
10. Dans notre configuration exemple, il s’agit du premier serveur d’un nouveau réseau. Choisir « Ajouter une nouvelle forêt » pour configurer un domaine neuf. Indiquer un Nom de domaine racine, par exemple domaine.local ou entreprise.local.

Capture

11. Laisser coché l’ajout de la fonctionnalité Serveur DNS pour ajouter ce rôle et indiquer un mot de passe de récupération des services d’annuaire (DSRM). Ce mot de passe ne doit absolument pas être perdu.

Capture

12. Un message d’erreur en jaune vient alerter de la délégation du serveur DNS. Il n’y a rien à faire à ce stade, cliquer simplement sur Suivant pour continuer.

Capture

13. Nous avons précédemment choisi un nom de domaine complet (FQDN), il faut maintenant indiquer l’équivalent NetBIOS pour les anciens appareils qui ne gèrent pas les noms de domaines qualifiés. Par exemple, pour « domaine.local » on pourra choisir le NetBIOS « DOMAINE » .

Capture

14. Valider l’emplacement de la base de données AD DS, des journaux d’historique et pour SYSVOL. Laisser les dossiers proposés par défaut (NTDS et SYSVOL dans C:\Windows).

CApture

15. Un récapitulatif résume la configuration qui va être appliquée. Cliquer sur Suivant pour continuer.

16. Une dernière vérification est effectuée, des notifications sont affichées mais cliquer sur Installer pour démarrer le processus.

Capture

17. L’opération dure quelques minutes et le redémarrage de Windows prendra plus de temps que d’habitude, le temps de configurer le contrôleur de domaine.

18. La connexion à Windows doit maintenant se faire sur le domaine pour utiliser le compte Administrateur du domaine. Utiliser le mot de passe du compte Administrateur créé lors de l’installation de Windows Server 2016.



