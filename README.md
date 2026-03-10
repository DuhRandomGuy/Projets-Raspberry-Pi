# Raspberry Pi Cyber-Lab
Bienvenue dans mon dépôt de mes projets avec mon Raspberry Pi. Ce projet regroupe mes différentes configurations de serveurs et d'outils réseau basés sur Raspberry Pi, avec une emphase particulière sur le durcissement système (Hardening) et la sécurisation des flux.

## Vue d'ensemble
L'objectif de ce laboratoire est de simuler un environnement d'entreprise sécurisé à petite échelle pour pratiquer l'administration système Linux, la gestion réseau et les concepts de cybersécurité.

## Projets inclus
NAS Sécurisé (OpenMediaVault)
Transformation d'un Raspberry Pi 5 en serveur de stockage robuste.

Technologies : OMV, SMB/NFS, RAID, EXT4.

Focus Sécurité : Gestion fine des ACLs (Access Control Lists), désactivation des services inutiles, et monitoring des logs d'accès.

Lien vers le dossier : /NAS-Storage

## Protection Réseau (Pi-hole)
Mise en place d'un pare-feu DNS pour l'ensemble du réseau local.

Technologies : DNS Sinkhole, FTL, Blocklists.

Focus Sécurité : Protection contre le pistage, blocage des domaines de télémétrie et réduction de la surface d'attaque publicitaire.

Lien vers le dossier : /Pi-hole-Security

## Comment utiliser ce dépôt ?
Chaque sous-dossier contient :

Un fichier README.md détaillé avec les étapes d'installation.

Les scripts de configuration (.sh) utilisés.

Les fichiers de configuration (.conf) anonymisés.
