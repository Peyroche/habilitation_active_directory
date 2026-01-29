# Projet 1 : Habilitation Active Directory

---

## I. Contexte :

Dans le cadre de ma formation en BTS SIO et de ma montée en compétences en administration système, j’ai choisi de mettre en place une infrastructure Active Directory complète afin de comprendre et maîtriser les mécanismes d’habilitation, de gestion des utilisateurs et de sécurisation des accès. L’objectif est de simuler un environnement de l'entreprise MDF comprenant deux services (Informatique, Comptabilité) et de mettre en œuvre une gestion des permissions conforme au modèle AGDLP. 

---

## II. Présentation de l’architecture : 

L’infrastructure se compose des éléments suivants : 

- serveur glpi dédié à la gestion du parc informatique et des tickets d’assistance. Il est intégré à l’infrastructure via le domaine Active Directory, permettant l’authentification centralisée des utilisateurs (SSO) et l’inventaire automatisé des postes grâce à l’agent GLPI. Ce serveur joue un rôle essentiel dans la supervision, la maintenance et la traçabilité des équipements du parc.

- serveur Windows Server jouant le rôle de contrôleur de domaine (DC). Il héberge les services essentiels : Active Directory Domain Services (AD DS), DNS, gestion des utilisateurs, des groupes et des stratégies de sécurité. 

- domaine Active Directory structuré selon une logique professionnelle. Le domaine permet l’authentification centralisée des utilisateurs et la gestion des permissions via le modèle AGDLP. 

- unités d’organisation (OU) permettant de structurer les utilisateurs, les groupes et les postes clients. Cette organisation facilite l’application de stratégies de groupe (GPO) et la gestion des habilitations. 

- groupes globaux (GG) représentant les rôles métiers (Ressources Humaines, Informatique, Comptabilité). Ils regroupent les utilisateurs selon leur fonction. 

- groupes locaux de domaine (DLG) associés aux ressources partagées. Ils reçoivent les permissions NTFS et SMB sur les dossiers du serveur. 

- postes clients Windows Pro intégrés au domaine. Ils permettent aux utilisateurs de se connecter avec leur compte AD et d’accéder aux ressources selon leurs droits. 

- dossiers partagés sur le serveur, organisés par service (Informatique, Comptabilité). Chaque dossier est protégé par des permissions adaptées au rôle des utilisateurs. 

---

## III. Réalisations : 

- installer Windows Server
- installer Domaine Active Directory,
- installer WampServer (Serveur GLPI),
- installer deux postes clients,
- créer des unités d’organisation, 
- créer des groupes globaux, 
- créer des groupes locaux de domaine,
- créer des utilisateurs,
- créer deux dossiers partages,
- Joindre les postes clients aux domaines.

---

## III.1. Installation Windows Server :

## Installation Windows Server :

<p align="center">

<img src="install_SRV/01.png" width="400">

<img src="install_SRV/02.png" width="400">

<img src="install_SRV/03.png" width="400">

<img src="install_SRV/04.png" width="400">

<img src="install_SRV/05.png" width="400">

<img src="install_SRV/06.png" width="400">

<img src="install_SRV/07.png" width="400">

<img src="install_SRV/08.png" width="400">

<img src="install_SRV/09.png" width="400">

<img src="install_SRV/10.png" width="400">

</p>

## Configuration Windows Server :

<p align="center">

<img src="config_SRV/01.png" width="400">

<img src="config_SRV/02.png" width="400">

<img src="config_SRV/03.png" width="400">

<img src="config_SRV/04.png" width="400">

<img src="config_SRV/05.png" width="400">

<img src="config_SRV/06.png" width="400">

</p>

## Configuration réseau Windows Server :

<p align="center">

<img src="reseau_SRV/01.png" width="400">

<img src="reseau_SRV/02.png" width="400">

<img src="reseau_SRV/03.png" width="400">

<img src="reseau_SRV/04.png" width="400">

<img src="reseau_SRV/05.png" width="400">

<img src="reseau_SRV/06.png" width="400">

</p>

---

## III.2. Installation Domaine Active Directory :

<p align="center">

<img src="install_AD/01.png" width="400">

<img src="install_AD/02.png" width="400">

<img src="install_AD/03.png" width="400">

<img src="install_AD/04.png" width="400">

<img src="install_AD/05.png" width="400">

<img src="install_AD/06.png" width="400">

<img src="install_AD/07.png" width="400">

<img src="install_AD/08.png" width="400">

<img src="install_AD/09.png" width="400">

<img src="install_AD/10.png" width="400">

<img src="install_AD/11.png" width="400">

<img src="install_AD/12.png" width="400">

<img src="install_AD/13.png" width="400">

<img src="install_AD/14.png" width="400">

<img src="install_AD/15.png" width="400">

<img src="install_AD/16.png" width="400">

<img src="install_AD/17.png" width="400">

<img src="install_AD/18.png" width="400">

<img src="install_AD/19.png" width="400">

</p>

---

## III.3. Installation Serveur GLPI :

<p align="center">

<img src="install_SRV_GLPI/01.png" width="400">

<img src="install_SRV_GLPI/02.png" width="400">

<img src="install_SRV_GLPI/03.png" width="400">

<img src="install_SRV_GLPI/04.png" width="400">

<img src="install_SRV_GLPI/05.png" width="400">

<img src="install_SRV_GLPI/06.png" width="400">

<img src="install_SRV_GLPI/07.png" width="400">

<img src="install_SRV_GLPI/08.png" width="400">

<img src="install_SRV_GLPI/09.png" width="400">

<img src="install_SRV_GLPI/10.png" width="400">

</p>

## Configuration réseau Serveur GLPI :

<p align="center">

<img src="reseau_SRV_GLPI/01.png" width="400">

<img src="reseau_SRV_GLPI/02.png" width="400">

<img src="reseau_SRV_GLPI/03.png" width="400">

<img src="reseau_SRV_GLPI/04.png" width="400">

<img src="reseau_SRV_GLPI/05.png" width="400">

<img src="reseau_SRV_GLPI/06.png" width="400">

</p>

---

## III.4. Installation Poste Client PC01 du Service IT :

<p align="center">

<img src="install_PC01/01.png" width="400">

<img src="install_PC01/02.png" width="400">

<img src="install_PC01/03.png" width="400">

<img src="install_PC01/04.png" width="400">

<img src="install_PC01/05.png" width="400">

<img src="install_PC01/06.png" width="400">

<img src="install_PC01/07.png" width="400">

<img src="install_PC01/08.png" width="400">

<img src="install_PC01/09.png" width="400">

<img src="install_PC01/10.png" width="400">

</p>

## Configuration Poste Client PC01 du Service_IT :

<p align="center">

<img src="config_PC01/01.png" width="400">

<img src="config_PC01/02.png" width="400">

<img src="config_PC01/03.png" width="400">

<img src="config_PC01/04.png" width="400">

<img src="config_PC01/05.png" width="400">

<img src="config_PC01/06.png" width="400">

</p>

## Configuration réseau Poste Client PC01 du Service_IT :

<p align="center">

<img src="reseau_PC01/01.png" width="400">

<img src="reseau_PC01/02.png" width="400">

<img src="reseau_PC01/03.png" width="400">

<img src="reseau_PC01/04.png" width="400">

<img src="reseau_PC01/05.png" width="400">

<img src="reseau_PC01/06.png" width="400">

</p>

---

## III.5. Installation Poste Client PC02 du Service_Compta :

<p align="center">

<img src="install_PC02/01.png" width="400">

<img src="install_PC02/02.png" width="400">

<img src="install_PC02/03.png" width="400">

<img src="install_PC02/04.png" width="400">

<img src="install_PC02/05.png" width="400">

<img src="install_PC02/06.png" width="400">

<img src="install_PC02/07.png" width="400">

<img src="install_PC02/08.png" width="400">

<img src="install_PC02/09.png" width="400">

<img src="install_PC02/10.png" width="400">

</p>

## Configuration Poste Client PC0é du Service_Compta :

<p align="center">

<img src="config_PC02/01.png" width="400">

<img src="config_PC02/02.png" width="400">

<img src="config_PC02/03.png" width="400">

<img src="config_PC02/04.png" width="400">

<img src="config_PC02/05.png" width="400">

<img src="config_PC02/06.png" width="400">

</p>

## Configuration réseau Poste Client PC02 du Service_Compta :

<p align="center">

<img src="reseau_PC02/01.png" width="400">

<img src="reseau_PC02/02.png" width="400">

<img src="reseau_PC02/03.png" width="400">

<img src="reseau_PC02/04.png" width="400">

<img src="reseau_PC02/05.png" width="400">

<img src="reseau_PC02/06.png" width="400">

</p>










