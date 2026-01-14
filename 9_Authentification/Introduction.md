# INTRODUCTION 

---

L’authentification des utilisateurs du domaine sur un poste client constitue une étape essentielle dans la mise en place d’un environnement Windows Server centralisé et sécurisé. Une fois le poste correctement configuré et joint au domaine, il devient possible pour les collaborateurs de se connecter à leur session en utilisant leurs identifiants Active Directory. Cette authentification centralisée permet de garantir une gestion cohérente des comptes, d’appliquer automatiquement les stratégies de groupe (GPO) et d’assurer un contrôle strict des accès aux ressources du réseau.

Dans la continuité du modèle AGDLP et du travail réalisé sur la création des comptes, des groupes et des habilitations, l’authentification au poste client permet de vérifier que l’infrastructure est opérationnelle et que la communication entre le poste et le contrôleur de domaine fonctionne correctement. Elle constitue également un point de validation essentiel : si l’utilisateur peut se connecter avec son compte du domaine, cela confirme que les services DNS, les stratégies de sécurité et la jonction au domaine sont correctement configurés.

---

## Procédure d'authentification :

La procédure utilisée est la suivante :

1. Démarrer le poste client joint au domaine. 

2. À l’écran de connexion, sélectionner Autre utilisateur. 

3. Saisir les identifiants d’un utilisateur du domaine : 

- Nom d’utilisateur : (ex : mdf\Placide) 

- Mot de passe : (celui défini dans Active Directory).

- Valider la connexion.









