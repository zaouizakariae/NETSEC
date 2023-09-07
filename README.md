# Introduction :

la présentation de la conception et la mise en place d'un réseau d'entreprise dans le cadre de mon stage chez Orange Cyber Defense en utilisant le logiciel Packat Tracer. L'objectif principal de ce projet est de créer un réseau qui respecte les bonnes pratiques de sécurité et intègre les solutions de sécurité recommandées par des organismes tels que le NIST, Cisco et Fortinet.

![dsaas](https://github.com/zaouizakariae/NETSEC/assets/85891554/cf3e50da-58d1-4304-b919-5b7a06dd684b)

## Conception du réseau

Un centre de support emploie 300 employés.
Premier étage- (Département des ressources humaines et de la logistique - 100 utilisateurs prévus).
Deuxième étage - (Département DSI - 100 utilisateurs prévus). 
Troisième étage - (Finance - 100 utilisateurs prévus, salle des serveurs - 10 appareils prévus).

![dsaas](https://github.com/zaouizakariae/NETSEC/assets/85891554/cf3e50da-58d1-4304-b919-5b7a06dd684b)

## Modèle à trois couches de Cisco

Couche de cœur
Couche de distribution
Couche d'accès


## ISPs (Fournisseurs d'accès Internet) :

Deux ISPs ont été mis en place pour assurer une redondance et une disponibilité maximale de la connectivité Internet.


## Firewall

Un pare-feu a été déployé entre les ISPs et la zone DMZ pour contrôler et filtrer le trafic entrant et sortant



##  Zone DMZ

La zone DMZ contient les serveurs web, les serveurs de messagerie et les serveurs HTTP accessibles depuis Internet.

## Core Routeurs

Deux routeurs de cœur ont été déployés pour assurer une connectivité redondante et gérer le routage interne du réseau.

## Multilayer Switches

Deux commutateurs multi-niveaux sont utilisés pour la distribution du trafic à travers le réseau

## Segmentation en sous-réseaux

Quatre sous-réseaux ont été créés pour les différentes entités de l'entreprise

# Configuration du réseau

Conception hiérarchique du réseau.
Connexion des appareils réseau avec un câblage correct.
Configuration des paramètres de base des appareils.
Création de VLAN et attribution des numéros de VLAN aux ports.
Découpage en sous-réseaux et attribution d'adresses IP.
Configuration du routage inter-VLAN sur les commutateurs multi-niveaux (interface virtuelle de commutation).
Configuration d'un serveur DHCP dédié pour fournir des adresses IP dynamiques.
Configuration de SSH pour un accès distant sécurisé.
Configuration d'OSPF en tant que protocole de routage.
Configuration du PAT (Translation d'adresses réseau) pour le partage d'adresses IP.
Configuration de listes de contrôle d'accès ACL standard et étendue.
Configuration de la sécurité des ports ou de la sécurité du commutateur sur les commutateurs.
Configuration du réseau sans fil (point d'accès Cisco).
Configuration des appareils hôtes.
Configuration des routeurs des fournisseurs d'accès.

# Allocation d'adresses IP :

![image (5)](https://github.com/zaouizakariae/NETSEC/assets/85891554/4c6bb35f-d427-402a-bbbd-135f2ecf1f21)

![image (6)](https://github.com/zaouizakariae/NETSEC/assets/85891554/f7cb67b9-2b05-49c6-b75d-0bb4b4de3ea8)

Entre routeurs et ISPs
Public adds : 195.136.17.0/30, 195.136.17.4/30, 195.136.17.8/30, 195.136.17.12/30

# Solutions de sécurité et bonnes pratiques

Authentification et gestion des accès
Contrôle d'accès et segmentation
NGFW
Surveillance et détection d'intrusion (xdr,edr,SIEM...)
Chiffrement et VPN
Sensibilisation à la sécurité

## Authentification et gestion des accès :

Les périphériques du réseau sont configurés avec des identifiants d'accès uniques et des mots de passe forts.
authentification basée sur le port 802.1X
Gestion des clés WPA

## Contrôle d'accès et segmentation :

Les listes de contrôle d'accès (ACL)
Ce lien contient mon rapport sur la configuration des acl : https://github.com/zaka1200/acl-network-sec/blob/main/README.md
Segmentation du réseau en utilisant des VLAN virtuels (VLAN)

## NGFW

pare-feux de nouvelle génération (NGFW) entre le coeur et les ISPs pour inspecter et filtrer le trafic entrant et sortant du réseau.

![image (7)](https://github.com/zaouizakariae/NETSEC/assets/85891554/c7619c0d-f2b8-4b47-9cd3-55942c24adc2)

## Surveillance et détection d'intrusion (xdr,edr,SIEM...) :

Les outils de surveillance réseau et des systèmes de détection d'intrusion (IDS) pour détecter les activités suspectes ou les tentatives d'intrusion. 
mise en place d'un SIEM qui collecte, agrège et analyse les journaux et les événements de sécurité provenant de différentes sources .

## Chiffrement et VPN

Utilisation des connexions VPN (Virtual Private Network)IPSec pour les communications entre les différents sites de l'entreprise ou pour les accès à distance.
Chiffrement des données transitant via les VPN pour empêcher toute interception ou compromission

![image (8)](https://github.com/zaouizakariae/NETSEC/assets/85891554/44abfa3e-fec7-49bc-837a-01fe4c9827e7)

## Sensibilisation à la sécurité

La sensibilisation à la sécurité est un élément crucial pour garantir la sécurité globale du réseau. 
Organisation régulière des sessions de formation et de sensibilisation à la sécurité pour tous les employés.

## Conclusion 

Le réseau d'entreprise conçu dans le cadre de ce projet respecte les bonnes pratiques de sécurité recommandées. En mettant en œuvre des solutions telles que l'authentification et la gestion des accès, le contrôle d'accès, la surveillance et la détection d'intrusion, le chiffrement et VPN, la gestion des correctifs, ainsi que la sensibilisation à la sécurité, le réseau est mieux préparé pour faire face aux menaces et aux attaques potentielles.

