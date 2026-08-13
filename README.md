# Homelab TSSR

![Status](https://img.shields.io/badge/Statut-En%20cours-yellow)\
\
![VMware](https://img.shields.io/badge/Hyperviseur-VMware%20Workstation%20Pro-Pro696969) ![Windows Server](https://img.shields.io/badge/OS-Windows%20Server-0078D6) ![Active Directory](https://img.shields.io/badge/Microsoft-Active%20Directory-0078D4) ![Windows 10](https://img.shields.io/badge/OS-Windows%2010-0078D6) ![Debian](https://img.shields.io/badge/OS-Debian-A81D33) ![PowerShell](https://img.shields.io/badge/Automatisation-PowerShell-5391FE) ![Samba](https://img.shields.io/badge/Serveur%20de%20fichiers-Samba-1F3B57) ![Zabbix](https://img.shields.io/badge/Supervision-Zabbix-D40000) ![pfSense](https://img.shields.io/badge/Pare--feu-pfSense-212121)

Documentation de mon homelab autodidacte, réalisé en vue d'un contrat de professionnalisation pour le titre **TSSR (Technicien Supérieur Systèmes et Réseaux)**.


## Objectifs du projet

Après un BAC+2 Développeur / Intégrateur Web (2017) et plusieurs expériences en développement web, j'ai choisi de me spécialiser en administration systèmes et réseaux. Ce homelab a pour but de :

- Mettre en pratique, de façon autodidacte, les compétences fondamentales d'un TSSR : réseaux, virtualisation, administration Windows et Linux, supervision, sauvegarde et sécurité
- Documenter une véritable montée en compétences, étape par étape, avec les difficultés rencontrées et ce qui en a été retenu — pas seulement une liste de technologies
- Servir de preuve concrète de motivation et d'autonomie technique auprès des entreprises, dans le cadre de ma recherche d'un contrat de professionnalisation


## Environnement du lab

L'ensemble de l'infrastructure est virtualisé sur un seul poste (PC personnel sous Windows 11), avec **VMware Workstation Pro 26H1** comme hyperviseur unique, réseau virtuel en mode **Pont (Bridge)**. Trois machines virtuelles principales composent le socle du lab :

| VM | Rôle |
|---|---|
| 🪟 **Windows Server 2025** | Contrôleur de domaine (Active Directory, GPO, supervision, sauvegarde) |
| 💻 **Windows 10 22H2** | Poste client, membre du domaine |
| 🐧 **Debian 13 netinst "Trixie"** | Serveur Linux (services, partage de fichiers Samba, supervision Zabbix) |


## Sommaire de l'arborescence

```
homelab-journey/
├── README.md                    → ce fichier : présentation, objectifs, sommaire
├── docs/                        → schémas réseau, captures d'écran
│
├── lab0-reseaux/
│   └── README.md                 → notes Cisco Networking Academy (bases réseau)
│
├── lab1-infrastructure/
│   ├── 1.1-hyperviseur/          → installation de VMware Workstation + configuration des 3 VM
│   ├── 1.2-active-directory/     → domaine AD, unités d'organisation, utilisateurs, jonction de la VM Windows 10 au domaine 
│   ├── 1.3-gpo/                  → stratégies de groupe
│   ├── 1.4-services-linux/       → services Linux (partage, web, etc.)
│   ├── 1.5-powershell/           → scripts et automatisation
│   ├── 1.6-serveur-fichiers/     → serveur de fichiers Samba
│   ├── 1.7-sauvegarde/           → politique de sauvegarde et tests de restauration
│   ├── 1.8-supervision/          → supervision avec Zabbix
│   └── 1.9-securite/             → VLAN, pare-feu, durcissement AD et Linux
│
└── lab2-pannes/
    └── README.md                 → scénarios de pannes, méthode de diagnostic et résolution
```

Chaque sous-dossier contient son propre `README.md` détaillant : l'objectif du lab, les étapes réalisées, les difficultés rencontrées et ce qui en a été retenu.


## Progression

- [x] Lab 0 — Fondamentaux réseau
- [x] Lab 1.1 — Hyperviseur (Windows Server, Windows 10, Debian installés et snapshotés)
- [x] Lab 1.2 — Active Directory (OU, utilisateurs, jonction de la VM Windows 10 au domaine)
- [x] Lab 1.3 — Mise en place GPO restrictions panneau de configuration étendu au 3 OU (RH, Communication, Marketing)
- [x] Lab 1.4 — Mise en place des services linux (SSH, Nginx, Chrony, UFW)
- [ ] Lab 1.5 — En cours
- [x] Lab 1.6 — Serveur Samba + GPO pour deployer automatiquement le lecteur mappé par OU 
- [ ] Lab 1.7 à 1.9 — En cours
- [ ] Lab 2 — Simulation de pannes

