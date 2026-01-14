# CREATION GG ET DLG

---

## Objectifs :

Cette fiche a pour objective d'expliquer la création des Groupes Globaux (GG) qui serviront à regrouper les utilisateurs selon leur service afin d’appliquer ensuite le modèle AGDLP. 

| Services              | OU_Groupes  | GG         | OU_Utilisateurs | Utilisateurs |
|-----------------------|-------------|------------|-----------------|--------------|
| Ressources Humaines   | GG          | GG_RH      | Utilisateur_RH  |  Placide     |
| Informatique          | GG          | GG_INF     | Utilisateur_INF |  Fortuné     |
| Comptabilité          | GG          | GG_CP      | Utilisateur_CP  |  Hugues      |

Mais aussi la création des Groupes Domaines Local (DLG) qui seront utilisés pour attribuer des permissions NTFS/SMB sur les dossiers partagés du serveur. 

| Services              | OU_Groupes | DLG       |
|-----------------------|------------|-----------|
| Ressources Humaines   | DLG        | DLG_RH    |
| Informatique          | DLG        | DLG_INF   |
| Comptabilité          | DLG        | DLG_CP    |

---

## Procédure création des GG :

La procédure utilisée est la suivante :

1. Naviguer jusqu’à l’OU du service concerné (ex : GG)

2. Clic droit → Nouveau → Groupe 

3. Renseigner : 

- Nom du Groupe Global (ex : GG_RH) 

- Portée : Global 

- Type : Sécurité 

4. Valider. 

---

## Démonstration création d'un GG_RH :

<p align="center">

<img src="images_2/images_GG_RH/01.png" width="350">

<img src="images_2/images_GG_RH/02.png" width="350">

<img src="images_2/images_GG_RH/03.png" width="350">

<img src="images_2/images_GG_RH/04.png" width="350">

<img src="images_2/images_GG_RH/05.png" width="350">

</p>

---

## Procédure création des DLG :

La procédure utilisée est la suivante  :

1. Naviguer jusqu’à l’OU du service concerné (ex : DLG)

2. Clic droit → Nouveau → Groupe 

3. Renseigner : 

- Nom du Groupe Global (ex : DLG_RH) 

- Portée : Local de domaine

- Type : Sécurité 

4. Valider. 

---

## Démonstration création d'un DLG_RH :

<p align="center">

<img src="images_3/images_DLG_RH/01.png" width="350">

<img src="images_3/images_DLG_RH/02.png" width="350">

<img src="images_3/images_DLG_RH/03.png" width="350">

</p>

---

## Procédure ajout des utilisateurs aux GG :

La procédure utilisée est la suivante :

1. Naviguer jusqu’à l’OU du service concerné (ex : Utilisateur_RH) 

2. Clic droit sur l’utilisateur (ex : Placide) 

3. Clic sur Ajouter au groupe 

4. Entrer le groupe global (ex : GG_RH) 

5. Valider.

---

## Démonstration ajout d'un utilisateur_RH au GG_RH :

<p align="center">

<img src="images_4/images_ajout_RH/01.png" width="350">

<img src="images_4/images_ajout_RH/02.png" width="350">

</p>

---

## Procédure ajout des GG aux DLG :

La procédure utilisée est la suivante :

1. Naviguer jusqu’à l’OU du service concerné (ex : GG) 

2. Clic droit sur le groupe global (ex : GG_RH)
 
3. Clic sur Ajouter au groupe 

4. Entrer le Groupe Domaine Local (ex : DLG_RH) 

5. Valider .

---

## Démonstration ajout d'un GG_RH au DLG_RH :

<p align="center">

<img src="images_5/images_ajout_GG_RH/01.png" width="350">

<img src="images_5/images_ajout_GG_RH/02.png" width="350">

</p>