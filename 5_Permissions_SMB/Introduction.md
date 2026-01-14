# INTRODUCTION

---

L’attribution des permissions SMB constitue une étape essentielle dans la gestion sécurisée des ressources partagées au sein d’un domaine Active Directory. Une fois les utilisateurs créés et organisés dans des groupes globaux (GG), puis associés à des groupes locaux de domaine (DLG), il devient nécessaire de définir précisément les droits d’accès aux dossiers partagés afin de garantir une utilisation conforme, sécurisée et cohérente des données de l’entreprise. Le protocole SMB (Server Message Block) permet de mettre à disposition des ressources réseau telles que des répertoires ou des fichiers, mais son efficacité repose sur une configuration rigoureuse des permissions.

Cette procédure s’inscrit directement dans la continuité du modèle AGDLP, où les groupes locaux de domaine portent les droits effectifs sur les ressources. L’objectif est d’éviter toute attribution directe de permissions aux utilisateurs, de centraliser la gestion des accès et de faciliter l’administration quotidienne. En appliquant les permissions SMB aux DLG, l’administrateur garantit une structure claire, évolutive et conforme aux bonnes pratiques professionnelles.

--- 

## Procédure attribution permissions SMB :

La procédure utilisée est la suivante :

1. Clic droit sur le dossier (ex : Dossier_RH)

2. Propriétés 

3. Onglet Partage 

4. Partage avancé 

5. Cocher Partager ce dossier 

6. Cliquer sur Autorisations 

7. Supprimer “Tout le monde” 

8. Ajouter le Groupe Domaine Local (ex : DLG_RH) 

9. Donner les droits associés au groupe. (ex : Full Control).

---

## Tableau récapitulatif :

| Dossiers     | OU_Groupes  | DLG      | Droits de partage SMB                                                                |
|--------------|-------------|----------|--------------------------------------------------------------------------------------|
| Dossier_RH   | DLG         | DLG_RH   | Full Control (Contrôle total) : Modification + gestion des permissions du partage.   | 
| Dossier_INF  | DLG         | DLG_INF  | Change (Modification) : Lecture + modification, suppression, création de fichiers.   |
| Dossier_CP   | DLG         | DLG_CP   | Read (Lecture) : L’utilisateur peut lire, ouvrir, lister les fichiers.               |
