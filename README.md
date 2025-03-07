# TP - Mise en place d'un serveur DHCP, DNS, HTTP(S) et SSH avec Cockpit sous Linux

## 📌 Objectif
Ce TP a pour but de vous guider dans la mise en place d'un serveur sous Linux intégrant plusieurs services réseau essentiels :
- **DHCP** : Attribution dynamique des adresses IP
- **DNS (BIND9)** : Résolution de noms de domaine
- **HTTP(S) (Apache2)** : Hébergement de sites web sécurisés avec HTTPS
- **SSH** : Accès sécurisé au serveur via authentification par clé
- **Cockpit** : Interface web pour l'administration

## 📂 Structure du projet
```
│── 📄 README.md 
│── 📂 Docs/ → (Pour la documentation et le PDF du TP)
│ ├── Tp_3_seances_Nowak_Patrick.pdf 
│── 📂 Configs/ → (Pour les fichiers de configuration des services)
│ ├── dhcp_server.network → (Fichier de config DHCP)
│ ├── dhcp_client.network → (Fichier de config client DHCP)
│ ├── named.conf.local → (Fichier de config du DNS BIND9)
│ ├── db.ynov.b2 → (Fichier de zone DNS)
│ ├── apache2_site3.conf → (VirtualHost Apache pour HTTPS)
│ ├── sshd_config → (Configuration SSH)
│── 📂 Captures/ → (Pour les captures d'écran des tests & validations)
│ ├── test_dhcp.png → (Test d'attribution d'IP par DHCP)
│ ├── test_dns.png → (Test de résolution DNS)
│ ├── test_https.png → (Accès sécurisé HTTPS)
│ ├── test_ssh.png → (Connexion SSH par clé)
│ ├── cockpit_interface.png → (Interface de Cockpit)
```

## 🛠️ Prérequis
Avant de commencer, assurez-vous d'avoir :
- Une machine virtuelle Linux (Debian/Ubuntu)
- Un accès root ou un utilisateur avec sudo
- Une connexion internet active

## 🚀 Étapes du TP
### 1️⃣ Installation et configuration du serveur DHCP
- Activation de **systemd-networkd** et **systemd-resolved**
- Création des fichiers de configuration pour le DHCP

### 2️⃣ Mise en place du serveur DNS (BIND9)
- Installation de BIND9
- Configuration des zones DNS
- Vérification et tests

### 3️⃣ Déploiement d'Apache2 avec HTTPS
- Activation de SSL et HTTP/2
- Création des VirtualHosts
- Génération et signature des certificats avec OpenSSL

### 4️⃣ Sécurisation avec SSH
- Génération de clés SSH
- Configuration pour interdire l'accès par mot de passe

### 5️⃣ Installation de Cockpit
- Installation et activation de Cockpit
- Configuration du firewall pour autoriser l'accès
---
🖥️ Projet réalisé dans le cadre d'un TP sur l'administration système et réseau.

