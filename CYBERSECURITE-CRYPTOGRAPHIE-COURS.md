<div align="center">

<a href="https://github.com/0xCyberLiTech/CRYPTOGRAPHIE/blob/main/CYBERSECURITE-CRYPTOGRAPHIE-COURS.md">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=32&pause=1000&color=D14A4A&center=true&vCenter=true&width=1000&lines=Cryptographie+%26+Cybersécurité;Chiffrement+Symétrique+%26+Asymétrique;Hachage+•+Signatures+•+Certificats;PCI+et+Bonnes+Pratiques;Protection+des+Données" alt="Typing SVG" />
</a>

<p align="center">
  <em>Un dépôt pédagogique autour des fondamentaux de la cybersécurité.</em><br>
  <b>📘 Apprentissage – 🔐 Sécurité – 🧠 Compréhension</b>
</p>

</div>

---

### 👨‍💻 **À propos de moi.**

> Ce dépôt constitue mon laboratoire numérique où je consigne rigoureusement mes apprentissages et expérimentations.
> Passionné par l'écosystème Linux et la cybersécurité, je documente mon parcours et mes projets sur mon GitHub.
> Vous y trouverez des guides pratiques sur la supervision (Zabbix, Nagios), la conteneurisation (Docker) et la sécurisation de serveurs Debian.
> Mon objectif : partager mes connaissances de manière claire et pédagogique.
> N'hésitez pas à y jeter un œil : https://github.com/0xcyberlitech

<p align="center">
  <a href="https://skillicons.dev">
    <img src="https://skillicons.dev/icons?i=linux,debian,bash,docker,nginx,grafana,prometheus,git,vim" />
  </a>
</p>

---

### 🎯 **Objectif de ce dépôt.**

> Ce dépôt a pour vocation de centraliser un ensemble de notions clés en cybersécurité. Il s’adresse aux passionnés, étudiants, et professionnels souhaitant mieux comprendre les menaces informatiques, apprendre  > à sécuriser leurs environnements et se familiariser avec les concepts et outils de défense.

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

```bash
# Chiffrement
openssl enc -aes-256-cbc -salt -in message.txt -out message.txt.enc

# Déchiffrement
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

```bash
# Générer un hash SHA256
sha256sum fichier.txt

# Générer un hash MD5 (moins sécurisé)
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

```bash
# 1. Générer une clé privée
openssl genrsa -out server.key 2048

# 2. Créer une demande de certificat (CSR)
openssl req -new -key server.key -out server.csr

# 3. Signer le certificat vous-même
openssl x509 -req -days 365 -in server.csr -signkey server.key -out server.crt
```

### 📘 Utilisation :
- Les fichiers `.crt` et `.key` peuvent être utilisés dans des services comme NGINX, Apache, ou Squid (SSL Bump).

---

## 🔐 Cours 6 : Chiffrement de disque ou de volume avec `cryptsetup`

### 🎯 Objectif :
Créer un volume chiffré sur un fichier ou une partition.

### 🛠️ Exemple avec un fichier :

```bash
# Créer un fichier de 100 Mo
dd if=/dev/zero of=volume.img bs=1M count=100

# Formater en LUKS (cryptage)
cryptsetup luksFormat volume.img

# Ouvrir et mapper le volume
cryptsetup open volume.img secretvolume

# Formater le volume en ext4
mkfs.ext4 /dev/mapper/secretvolume

# Monter le volume
mount /dev/mapper/secretvolume /mnt
```

### 🔐 Pour fermer :

```bash
umount /mnt
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
  <b>🔒 Un guide proposé par <a href="https://github.com/0xCyberLiTech">0xCyberLiTech</a> • Pour des tutoriels accessibles à tous. 🔒</b>
</p>
