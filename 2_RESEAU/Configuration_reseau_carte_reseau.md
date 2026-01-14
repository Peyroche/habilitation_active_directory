# CONFIGURATION RESEAU INTERNE ET CARTES RESEAUX

---

## Objectif :

Cette fiche a pour objective d'expliquer comment configurer un réseau interne afin de permettre aux postes clients de communiquer avec le server du domaine Active Directory.

| Services métiers     | Postes clients      | IP         |  Masque        |  Passerelle    | Serveur DNS         |
|----------------------|---------------------|------------|----------------|----------------|---------------------|
| Ressources Humaines  | PC_RH Windows 10    | 10.0.0.20  | 255.255.255.0  |      /         |   10.0.0.10         | 
| Informatique         | PC_INF Windows 10   | 10.0.0.30  | 255.255.255.0  |      /         |   10.0.0.10         |
| Comptabilité         | PC_CP Windows 10    | 10.0.0.40  | 255.255.255.0  |      /         |   10.0.0.10         |


| Autres Services      | Serveur             | IP         | Masque         | Passerelle     | Serveur DNS         |
|----------------------|---------------------|------------|----------------|----------------|---------------------|
| Administration       | Windows server 22   | 10.0.0.10  | 255.255.255.0  |      /         |   10.0.0.10         |                     

---

## Procédure configuration des cartes réseaux :

La procédure utilisée est la suivante :

1. Ouvrir VirtualBox

2. Choix de la machine ( ex : Poste client Windows 10, Windows Server 22)

3. Onglet Réseau 

- Coche la case "Activer l’interface réseau" 

- Mode d’accès réseau : Réseau interne 

- Nom : intnet

- Type d’interface : Intel PRO/1000 MT Desktop (82540EM)

- Câble branché : coché ✅ 

---

## Démonstration configuration carte réseau Windows server 22 :

<p align="center">

<img src="images_1/images_carte/01.png" width="350">

<img src="images_1/images_carte/02.png" width="350">

</p>

---

## Démonstration configuration carte réseau d'un poste client PC_RH Windows 10 :

<p align="center">

<img src="images_2/images_carte/01.png" width="350">

<img src="images_2/images_carte/02.png" width="350">

</p>

---

## Procédure configuration réseau interne :

La procédure utilisée est la suivante :

1. Se connecter aux machines (ex : Windows server 22, PC_RH Windows 10)

2. Accéder au panneau de configuration

3. Réseau et Internet

4. Centre de partage et réseau

5. Ethernet

6. Protocole Internet version 4 (TCP/IPv4)

7. Configurer le réseau :

- Adresse IP

- Masque

- Passerelle

- Server DNS.

---

## Démonstration configuration Windows server 22 :

<p align="center">

<img src="images_3/images_conf_admin/01.png" width="350">

<img src="images_3/images_conf_admin/02.png" width="350">

<img src="images_3/images_conf_admin/03.png" width="350">

<img src="images_3/images_conf_admin/04.png" width="350">

<img src="images_3/images_conf_admin/05.png" width="350">

<img src="images_3/images_conf_admin/06.png" width="350">

<img src="images_3/images_conf_admin/07.png" width="350">

<img src="images_3/images_conf_admin/08.png" width="350">

<img src="images_3/images_conf_admin/09.png" width="350">

<img src="images_3/images_conf_admin/10.png" width="350">

</p>

---

## Démonstration configuration d'un poste client PC_RH Windows 10 :

<p align="center">

<img src="images_4/images_conf_user/01.png" width="350">

<img src="images_4/images_conf_user/02.png" width="350">

<img src="images_4/images_conf_user/03.png" width="350">

<img src="images_4/images_conf_user/04.png" width="350">

<img src="images_4/images_conf_user/05.png" width="350">

<img src="images_4/images_conf_user/06.png" width="350">

<img src="images_4/images_conf_user/07.png" width="350">

<img src="images_4/images_conf_user/08.png" width="350">

<img src="images_4/images_conf_user/09.png" width="350">

<img src="images_4/images_conf_user/10.png" width="350">

</p>

---

## Test après configuration d'un poste client PC_RH Windows 10 :

Avant toute tentative de joindre le domaine, il faut s’assurer que le poste client peut communiquer avec le contrôleur de domaine. On test la configuration réseau du poste client dans l'invite de commande :
 
- ipconfig : Pour confirmer que le poste client a une adresse IP dans le même réseau que le serveur. Pour Vérifier que le DNS pointe vers le contrôleur de domaine.

- Ping 10.0.0.10 : Pour vérifier que le poste client peut joindre le serveur. Pour confirmer que les deux machines sont dans le même réseau VirtualBox. Pour s’assurer que le serveur est allumé et que le pare‑feu ne bloque pas ICMP.

<p align="center">

<img src="images_5/images_verifica/01.png" width="350">

</p>