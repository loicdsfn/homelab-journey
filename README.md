\# 🖥️ Homelab TSSR



!\[Status](https://img.shields.io/badge/Statut-En%20cours-yellow)

!\[VMware](https://img.shields.io/badge/Hyperviseur-VMware%20Workstation-696969)

!\[Windows Server](https://img.shields.io/badge/OS-Windows%20Server-0078D6)

!\[Debian](https://img.shields.io/badge/OS-Debian-A81D33)

!\[Zabbix](https://img.shields.io/badge/Supervision-Zabbix-D40000)



Documentation de mon homelab autodidacte, réalisé en vue d'un contrat de professionnalisation pour le titre \*\*TSSR (Technicien Supérieur Systèmes et Réseaux)\*\*.



\## 🎯 Objectifs du projet



Après un BAC+2 Développeur / Intégrateur Web (2017) et plusieurs expériences en développement web, j'ai choisi de me spécialiser en administration systèmes et réseaux. Ce homelab a pour but de :



\- Mettre en pratique, de façon autodidacte, les compétences fondamentales d'un TSSR : réseaux, virtualisation, administration Windows et Linux, supervision, sauvegarde et sécurité

\- Documenter une véritable montée en compétences, étape par étape, avec les difficultés rencontrées et ce qui en a été retenu — pas seulement une liste de technologies

\- Servir de preuve concrète de motivation et d'autonomie technique auprès des entreprises, dans le cadre de ma recherche d'un contrat de professionnalisation



\## 🧱 Environnement du lab



L'ensemble de l'infrastructure est virtualisé sur un seul poste (PC personnel sous Windows 11), avec \*\*VMware Workstation Pro\*\* comme hyperviseur unique. Trois machines virtuelles principales composent le socle du lab :



| VM | Rôle |

|---|---|

| 🪟 \*\*Windows Server\*\* | Contrôleur de domaine (Active Directory, GPO, supervision, sauvegarde) |

| 💻 \*\*Windows 11\*\* | Poste client, membre du domaine |

| 🐧 \*\*Debian\*\* | Serveur Linux (services, partage de fichiers Samba, supervision Zabbix) |



\## 🗂️ Sommaire de l'arborescence



```

homelab-tssr/

├── README.md                    → ce fichier : présentation, objectifs, sommaire

├── docs/                        → schémas réseau, captures d'écran

│

├── lab0-reseaux/

│   └── README.md                 → notes Cisco Networking Academy (bases réseau)

│

├── lab1-infrastructure/

│   ├── 1.1-hyperviseur/          → installation et configuration de VMware Workstation

│   ├── 1.2-windows-server/       → déploiement de Windows Server

│   ├── 1.3-active-directory/     → domaine AD, unités d'organisation, utilisateurs

│   ├── 1.4-gpo/                  → stratégies de groupe

│   ├── 1.5-linux/                → installation et administration Debian

│   ├── 1.6-services-linux/       → services Linux (partage, web, etc.)

│   ├── 1.7-powershell/           → scripts et automatisation

│   ├── 1.8-serveur-fichiers/     → serveur de fichiers Samba

│   ├── 1.9-sauvegarde/           → politique de sauvegarde et tests de restauration

│   ├── 1.10-supervision/         → supervision avec Zabbix

│   └── 1.11-securite/            → VLAN, pare-feu, durcissement AD et Linux

│

└── lab2-pannes/

&#x20;   └── README.md                 → scénarios de pannes, méthode de diagnostic et résolution

```



Chaque sous-dossier contient son propre `README.md` détaillant : l'objectif du lab, les étapes réalisées, les difficultés rencontrées et ce qui en a été retenu.



\## 📈 Progression



\- \[x] Lab 0 — Fondamentaux réseau

\- \[x] Lab 1.1 — Hyperviseur

\- \[ ] Lab 1.2 à 1.11 — En cours

\- \[ ] Lab 2 — Simulation de pannes

