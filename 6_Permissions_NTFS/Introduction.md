# INTRODUCTION

---

L’attribution des permissions NTFS constitue une étape fondamentale dans la sécurisation et l’organisation des accès aux données au sein d’un système d’information. Alors que les permissions SMB contrôlent l’accès aux partages réseau, les permissions NTFS définissent précisément ce que chaque utilisateur ou groupe peut faire à l’intérieur même du système de fichiers : lecture, modification, suppression ou gestion avancée des dossiers et fichiers. Cette granularité permet d’assurer une protection fine des données et de garantir que chaque collaborateur dispose uniquement des droits nécessaires à l’exercice de ses fonctions.

Dans la continuité du modèle AGDLP mis en place dans l’infrastructure Active Directory, les permissions NTFS sont attribuées non pas directement aux utilisateurs, mais aux groupes locaux de domaine (DLG). Cette méthode permet de centraliser la gestion des droits, d’éviter les erreurs d’attribution individuelle et de faciliter l’administration du domaine. Les groupes globaux (GG), qui regroupent les utilisateurs selon leur rôle ou leur service, sont ensuite intégrés dans les DLG, lesquels portent les permissions effectives sur les dossiers. Cette séparation claire entre identité et autorisation garantit une structure cohérente, évolutive et conforme aux bonnes pratiques professionnelles.

---

## Procédure permissions NTFS :

La procédure utilisée est la suivante :

1. Clic droit sur le dossier (ex : Dossier_RH)

2. Propriétés

3. Onglet sécurité

4. Cliquer sur Modifier

5. Ajouter le Groupe Domaine Local (ex : DLG_RH)

6. Donner les droits associés au groupe. (ex : Change).

---

## Tableau récapitulatif :

| Dossiers     | OU_Groupes | DLG     | Permissions NTFS                                                                     |
|--------------|------------|---------|--------------------------------------------------------------------------------------|
| Dossier_RH   | DLG        | DLG_RH  | Change (Modification) : Lecture + modification, suppression, création de fichiers.   | 
| Dossier_INF  | DLG        | DLG_INF | Read (Lecture) : L’utilisateur peut lire, ouvrir, lister les fichiers.               |
| Dossier_CP   | DLG        | DLG_CP  | Read (Lecture) : L’utilisateur peut lire, ouvrir, lister les fichiers.               |
