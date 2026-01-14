# INTRODUCTION

---

La configuration réseau interne constitue une étape fondamentale dans la mise en place d’une infrastructure Windows Server fonctionnelle et cohérente. Avant de pouvoir intégrer un poste client au domaine, appliquer des stratégies de groupe ou accéder aux services proposés par le serveur, il est indispensable d’établir une communication réseau stable, structurée et correctement paramétrée entre les différentes machines du système d’information. Cette configuration garantit que le poste client peut identifier le serveur, résoudre son nom via DNS, communiquer avec lui et accéder aux services essentiels tels que l’authentification ou le partage de ressources.

Dans le cadre de ce projet, la configuration réseau interne permet de définir les adresses IP, le masque de sous‑réseau, la passerelle éventuelle et surtout le serveur DNS, qui joue un rôle central dans le fonctionnement d’Active Directory. Une mauvaise configuration réseau peut empêcher la jonction au domaine, bloquer les stratégies de groupe ou rendre les services du serveur inaccessibles. Il est donc essentiel de mettre en place un paramétrage rigoureux et conforme aux bonnes pratiques.

---

## Procédure de configuration carte réseau :

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

## Procédure de configuration réseau interne :

La procédure utilisée est la suivante :

1. Se connecter aux machines Windows server et postes clients (ex : PC_RH Windows 10)

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

## Tableau récapitulatif :

| Services métiers     | Postes clients      | IP         |  Masque        |  Passerelle    | Serveur DNS         |
|----------------------|---------------------|------------|----------------|----------------|---------------------|
| Ressources Humaines  | PC_RH Windows 10    | 10.0.0.20  | 255.255.255.0  |      /         |   10.0.0.10         | 
| Informatique         | PC_INF Windows 10   | 10.0.0.30  | 255.255.255.0  |      /         |   10.0.0.10         |
| Comptabilité         | PC_CP Windows 10    | 10.0.0.40  | 255.255.255.0  |      /         |   10.0.0.10         |


| Autres Services      | Serveur             | IP         | Masque         | Passerelle     | Serveur DNS         |
|----------------------|---------------------|------------|----------------|----------------|---------------------|
| Administration       | Windows server 22   | 10.0.0.10  | 255.255.255.0  |      /         |   10.0.0.10         |                     

---

## Procédure test configuration Postes clients :

On test la configuration réseau du poste client dans l'invite de commande :
 
- ipconfig : Pour confirmer que le poste client a une adresse IP dans le même réseau que le serveur. Pour Vérifier que le DNS pointe vers le contrôleur de domaine.

- Ping 10.0.0.10 : Pour vérifier que le poste client peut joindre le serveur. Pour confirmer que les deux machines sont dans le même réseau VirtualBox. Pour s’assurer que le serveur est allumé et que le pare‑feu ne bloque pas ICMP.

