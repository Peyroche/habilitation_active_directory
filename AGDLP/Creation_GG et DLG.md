# CREATION GG ET DLG

---

## Objectif :

Le groupe global (GG) représente le rôle métier dans l’entreprise. Il sert à regrouper les utilisateurs selon leur service afin d’appliquer ensuite le modèle AGDLP. 
Tandis que Le groupe domaine local (DLG) est utilisé pour attribuer les permissions NTFS et SMB sur le dossier partagé du serveur. 

---

## Procédure :

La procédure utilisée est la suivante  :

Créer un groupe global

1. Aller dans : OU_Groupes → GG 

2. Clic droit → Nouveau → Groupe 

3. Renseigner : 

- Nom du Groupe Global (ex : GG_RH) 

- Portée : Global 

- Type : Sécurité 

4. Valider. 


Ensuite Ajouter l'utilisateur au groupe global

5. Aller dans l’OU contenant l’utilisateur (ex : Utilisateurs_RH) 

6. Clic droit sur l’utilisateur (ex : Placide) 

7. Sélectionner Ajouter au groupe 

8. Entrer le groupe global (ex : GG_RH) 

9. Valider.


Ensuite créer un groupe domaine local

10. Aller dans : OU_Groupes → DLG

11. Clic droit → Nouveau → Groupe 

12. Renseigner : 

- Nom du Groupe Domaine Local (ex : DLG_RH) 

- Portée : Local de domaine 

- Type : Sécurité 

13. Valider.


Ensuite ajouter le groupe global au groupe domaine local

14. Aller dans : OU_Groupes → GG 

15. Clic droit sur le groupe global (ex : GG_RH)
 
16. Sélectionner Ajouter au groupe 

17. Entrer le Groupe Domaine Local (ex : DLG_RH) 

18. Valider.

---

## Démonstration : 

Créer un groupe global

<p align="center">

<img src="images/07.png" width="400">

<img src="images/08.png" width="400">

<img src="images/09.png" width="400">

<img src="images/10.png" width="400">

</p>


Ensuite ajouter l'utilisateur au groupe global

<p align="center">

<img src="images/11.png" width="400">

<img src="images/12.png" width="400">

</p>


Ensuite créer un groupe domaine local

<p align="center">

<img src="images/13.png" width="400">

<img src="images/14.png" width="400">

<img src="images/15.png" width="400">

</p>


Ensuite ajouter le groupe global au groupe domaine local

<p align="center">

<img src="images/16.png" width="400">

<img src="images/17.png" width="400">

</p>









