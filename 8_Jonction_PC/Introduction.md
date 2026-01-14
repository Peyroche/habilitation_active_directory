# INTRODUCTION

---

La jonction d’un poste client au domaine Active Directory constitue une étape essentielle dans la mise en place d’un environnement réseau centralisé et sécurisé. Elle permet d’intégrer l’ordinateur dans l’infrastructure du système d’information afin qu’il puisse bénéficier des services fournis par le contrôleur de domaine, tels que l’authentification centralisée, l’application des stratégies de groupe (GPO), la gestion des habilitations ou encore l’accès aux ressources partagées. Sans cette intégration, le poste fonctionnerait de manière isolée, sans contrôle ni cohérence avec les règles définies au niveau du domaine.

Dans la continuité du modèle AGDLP et du travail réalisé sur la création des comptes utilisateurs et des groupes, la jonction du poste client permet d’associer chaque machine à l’annuaire Active Directory. Cette étape garantit que les utilisateurs pourront se connecter avec leurs identifiants du domaine, que les permissions NTFS et SMB seront correctement appliquées et que les stratégies de sécurité définies par l’administrateur seront automatiquement déployées. Elle constitue ainsi un prérequis indispensable pour assurer une gestion centralisée, homogène et professionnelle du parc informatique.

---

## Procédure jonction des postes clients au domaine :

La procédure utilisée est la suivante :

1. Se connecter à Windows server 22

2. Dans le gestionnaire de fichier, clic droit sur PC 

2. Cliquer sur propriété 

3. Ensuite cliquer sur renommer ce PC

4. Modifier

5. Entrer un domaine : mdf.corp 

6. Fournir :

- Un compte admin du domaine (ex : Administrateur)

- Mot de passe du domaine

7. Redémarrer le poste client.