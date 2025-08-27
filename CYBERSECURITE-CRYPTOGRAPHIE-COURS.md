<div align="center">

  <br></br>
  
  <a href="https://github.com/0xCyberLiTech">
    <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&size=50&duration=6000&pause=1000000000&color=FF0048&center=true&vCenter=true&width=1100&lines=%3ECRYPTOGRAPHIE_" alt="Titre dynamique CRYPTOGRAPHIE" />
  </a>
  
  <br></br>

  <h2>Laboratoire numérique pour la cybersécurité, Linux & IT</h2>

  <p align="center">
    <a href="https://0xcyberlitech.github.io/">
      <img src="https://img.shields.io/badge/Portfolio-0xCyberLiTech-181717?logo=github&style=flat-square" alt="🌐 Portfolio" />
    </a>
    <a href="https://github.com/0xCyberLiTech">
      <img src="https://img.shields.io/badge/Profil-GitHub-181717?logo=github&style=flat-square" alt="🔗 Profil GitHub" />
    </a>
    <a href="https://github.com/0xCyberLiTech/CRYPTOGRAPHIE/releases/latest">
      <img src="https://img.shields.io/github/v/release/0xCyberLiTech/CRYPTOGRAPHIE?label=version&style=flat-square&color=blue" alt="📦 Dernière version" />
    </a>
    <a href="https://github.com/0xCyberLiTech/CRYPTOGRAPHIE/blob/main/CHANGELOG.md">
      <img src="https://img.shields.io/badge/📄%20Changelog-CRYPTOGRAPHIE-blue?style=flat-square" alt="📄 CHANGELOG CRYPTOGRAPHIE" />
    </a>
    <a href="https://github.com/0xCyberLiTech?tab=repositories">
      <img src="https://img.shields.io/badge/Dépôts-publics-blue?style=flat-square" alt="📂 Dépôts publics" />
    </a>
    <a href="https://github.com/0xCyberLiTech/CRYPTOGRAPHIE/graphs/contributors">
      <img src="https://img.shields.io/badge/👥%20Contributeurs-cliquez%20ici-007ec6?style=flat-square" alt="👥 Contributeurs CRYPTOGRAPHIE" />
    </a>
  </p>

</div>

<!--
Optimisation SEO : mots-clés cybersécurité, Linux, administration système, sécurité informatique, tutoriels, guides, expertise, formation, supervision, Docker, OpenVAS, firewall, proxy, DNS, SSH, Debian, IT, réseau, cryptographie, open source, ressources techniques, étudiants, professionnels, passionnés.
-->

<div align="center">
  <img src="https://img.icons8.com/fluency/96/000000/cyber-security.png" alt="CyberSec" width="80"/>
</div>

<div align="center">
  <p>
    <strong>Cybersécurité</strong> <img src="https://img.icons8.com/color/24/000000/lock--v1.png"/> • <strong>Linux Debian</strong> <img src="https://img.icons8.com/color/24/000000/linux.png"/> • <strong>Sécurité informatique</strong> <img src="https://img.icons8.com/color/24/000000/shield-security.png"/>
  </p>
</div>

---

## 🚀 À propos & Objectifs

Ce projet propose des solutions innovantes et accessibles en cybersécurité, avec une approche centrée sur la simplicité d’utilisation et l’efficacité. Il vise à accompagner les utilisateurs dans la protection de leurs données et systèmes, tout en favorisant l’apprentissage et le partage des connaissances.

Le contenu est structuré, accessible et optimisé SEO pour répondre aux besoins de :
- 🎓 Étudiants : approfondir les connaissances
- 👨‍💻 Professionnels IT : outils et pratiques
- 🖥️ Administrateurs système : sécuriser l’infrastructure
- 🛡️ Experts cybersécurité : ressources techniques
- 🚀 Passionnés du numérique : explorer les bonnes pratiques

---

# 🔐 Cours complet : Introduction à la cryptographie sous Debian 12

Ce document propose une série de mini-cours pour comprendre et pratiquer la **cryptographie** dans un environnement **Linux Debian 12**. Chaque section contient une explication théorique claire et des exercices pratiques.

---

## 📚 Cours 1 : Introduction à la cryptographie

### 🧠 Définition
La cryptographie est l'art de **protéger l'information** contre les accès non autorisés, en transformant les données (texte clair) en un format illisible (texte chiffré), et inversement.

### 🔍 Objectifs principaux :
- **Confidentialité** : empêcher la lecture non autorisée.
- **Authenticité** : prouver l'identité de l’émetteur.
- **Intégrité** : garantir que les données n'ont pas été modifiées.
- **Non-répudiation** : empêcher qu’un émetteur nie l’avoir fait.

### 🧱 Types de cryptographie :
- **Symétrique** : une seule clé pour chiffrer/déchiffrer.
- **Asymétrique** : paire de clés publique/privée.
- **Hachage** : générer une empreinte unique (non réversible).

---

## 🧪 Cours 2 : Chiffrement symétrique avec OpenSSL

### 🎯 Objectif :
Chiffrer un fichier avec une clé partagée (symétrique), puis le déchiffrer.

### 📌 Commandes de base :

### Déchiffrement
```bash
openssl enc -aes-256-cbc -salt -in message.txt -out message.txt.enc
```

### Déchiffrement
```bash
openssl enc -aes-256-cbc -d -in message.txt.enc -out message-decrypted.txt
```

### 📘 Explications :
- `-aes-256-cbc` : algorithme de chiffrement (256 bits).
- `-salt` : ajoute une protection contre les attaques par dictionnaire.
- Il vous sera demandé un mot de passe au moment du chiffrement/déchiffrement.

---

## 🔐 Cours 3 : Cryptographie asymétrique avec GPG

### 🎯 Objectif :
Créer une paire de clés, chiffrer des fichiers avec une clé publique et les déchiffrer avec la clé privée.

### 🛠️ Génération des clés :

```bash
gpg --full-generate-key
```

Suivre les étapes pour créer une clé RSA (2048 ou 4096 bits).

### 📤 Export de la clé publique :

```bash
gpg --armor --export votreadresse@mail.com > public.key
```

### 🔒 Chiffrement :

```bash
gpg --encrypt --recipient votreadresse@mail.com fichier.txt
```

### 🔓 Déchiffrement :

```bash
gpg --output fichier.txt --decrypt fichier.txt.gpg
```

### ✅ Avantages :
- Pas besoin de partager de mot de passe.
- La signature numérique peut être ajoutée pour l’authenticité.

---

## 🔎 Cours 4 : Vérification d’intégrité avec le hachage

### 🎯 Objectif :
Créer une empreinte numérique d’un fichier et la vérifier après un transfert.

### 🔧 Commandes utiles :


### Générer un hash SHA256
```bash
sha256sum fichier.txt
```

### Générer un hash MD5 (moins sécurisé)
```bash
md5sum fichier.txt
```

### 📘 Utilisation :
- Transmettez le fichier + son hash.
- L’utilisateur compare le hash généré en local avec celui fourni.

---

## 🛠️ Cours 5 : Certificats SSL avec OpenSSL

### 🎯 Objectif :
Générer un certificat SSL auto-signé (utile pour un serveur local ou un proxy interceptant).

### 🔧 Étapes :


### 1. Générer une clé privée
```bash
openssl genrsa -out server.key 2048
```
### 2. Créer une demande de certificat (CSR)

```bash
openssl req -new -key server.key -out server.csr
```

### 3. Signer le certificat vous-même
```bash
openssl x509 -req -days 365 -in server.csr -signkey server.key -out server.crt
```

### 📘 Utilisation :
- Les fichiers `.crt` et `.key` peuvent être utilisés dans des services comme NGINX, Apache, ou Squid (SSL Bump).

---

## 🔐 Cours 6 : Chiffrement de disque ou de volume avec `cryptsetup`

### 🎯 Objectif :
Créer un volume chiffré sur un fichier ou une partition.

### 🛠️ Exemple avec un fichier :

### Créer un fichier de 100 Mo
```bash
dd if=/dev/zero of=volume.img bs=1M count=100
```
### Formater en LUKS (cryptage)
```bash
cryptsetup luksFormat volume.img
```
### Ouvrir et mapper le volume
```bash
cryptsetup open volume.img secretvolume
```
### Formater le volume en ext4
```bash
mkfs.ext4 /dev/mapper/secretvolume
```
### Monter le volume
```bash
mount /dev/mapper/secretvolume /mnt
```

### 🔐 Pour fermer :

```bash
umount /mnt
```

```bash
cryptsetup close secretvolume
```

---

## 🔑 Cours 7 : Gestion sécurisée des mots de passe avec `pass`

### 🎯 Objectif :
Gérer ses mots de passe chiffrés localement avec GPG.

### 🛠️ Installation :

```bash
sudo apt install pass
```

### 🧾 Initialisation avec votre clé GPG :

```bash
pass init "Nom ou email associé à la clé GPG"
```

### ➕ Ajouter un mot de passe :

```bash
pass insert github.com/email@example.com
```

### 🔍 Lire un mot de passe :

```bash
pass github.com/email@example.com
```

---

## 📊 Récapitulatif des outils

| Objectif | Outil | Commande clé |
|---------|-------|---------------|
| Chiffrement symétrique | `openssl` | `openssl enc` |
| Chiffrement asymétrique | `gpg` | `gpg --encrypt` |
| Hachage / intégrité | `sha256sum` | `sha256sum fichier` |
| Certificat SSL | `openssl` | `openssl req`, `openssl x509` |
| Volume chiffré | `cryptsetup` | `cryptsetup luksFormat` |
| Gestion mots de passe | `pass` + `gpg` | `pass insert` |

---

## 🎯 Pour aller plus loin :

- Étudier **PGP** (OpenPGP standard)
- Utiliser **YubiKey** pour protéger les clés GPG
- Apprendre à configurer **SSL sur NGINX ou Squid Proxy**
- Utiliser **Tails** ou **Qubes OS** pour un usage orienté sécurité

---

<p align="center">
  <a href="https://github.com/0xCyberLiTech" target="_blank" rel="noopener">
    <img src="https://skillicons.dev/icons?i=linux,debian,bash,docker,nginx,git,vim,python,markdown" alt="Skills" width="420">
  </a>
</p>

<p align="center">
  <b>🔒 Un guide proposé par <a href="https://github.com/0xCyberLiTech">0xCyberLiTech</a> • Pour des tutoriels accessibles à tous. 🔒</b>
</p>
