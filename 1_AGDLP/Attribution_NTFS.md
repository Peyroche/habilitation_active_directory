# ATTRIBUTIONS DES PERMISSIONS NTFS

---

## Objectif :

Cette fiche a pour objective d'expliquer comment attribuer aux Groupes du Domaine Local (DLG) les permissions NTFS sur des dossiers.

| Dossiers     | OU_Groupes | DLG     | Permissions NTFS                                                                     |
|--------------|------------|---------|--------------------------------------------------------------------------------------|
| Dossier_RH   | DLG        | DLG_RH  | Change (Modification) : Lecture + modification, suppression, création de fichiers.   | 
| Dossier_INF  | DLG        | DLG_INF | Read (Lecture) : L’utilisateur peut lire, ouvrir, lister les fichiers.               |
| Dossier_CP   | DLG        | DLG_CP  | Read (Lecture) : L’utilisateur peut lire, ouvrir, lister les fichiers.               |

---

## Procédure attribution des permissions NTFS aux DLG sur des dossiers :

La procédure utilisée est la suivante :

1. Clic droit sur le dossier (ex : Dossier_RH)

2. Propriétés

3. Onglet sécurité

4. Cliquer sur Modifier

5. Ajouter le Groupe Domaine Local (ex : DLG_RH)

6. Donner les droits associés au groupe. (ex : Change).

---

## Démonstration d'une attribution des permissions NTFS au DLG_RH sur un Dossier_RH: 

<p align="center">

<img src="images_7/images_NTFS_RH/01.png" width="350">

<img src="images_7/images_NTFS_RH/02.png" width="350">

<img src="images_7/images_NTFS_RH/03.png" width="350">

<img src="images_7/images_NTFS_RH/04.png" width="350">

<img src="images_7/images_NTFS_RH/05.png" width="350">

<img src="images_7/images_NTFS_RH/06.png" width="350">

<img src="images_7/images_NTFS_RH/07.png" width="350">

<img src="images_7/images_NTFS_RH/08.png" width="350">

<img src="images_7/images_NTFS_RH/09.png" width="350">

</p>