<!-- MASTER-HEADER-START -->
<div align="center">

<a href="https://0xcyberlitech.com/">
  <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/headers/header-cryptographie.svg" alt="ATELIER CRYPTOGRAPHIE // PKI & TLS" width="100%" />
</a>

<p align="center">
  <a href="https://0xcyberlitech.com/"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-portal.svg" alt="Portail 0xCyberLiTech.com" width="24%" /></a>
  <a href="https://0xcyberlitech.com/soc-rd.html"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-soc-rd.svg" alt="Livre Blanc SOC Cockpit" width="24%" /></a>
  <a href="https://0xcyberlitech.com/jarvis-rd.html"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-jarvis-rd.svg" alt="Livre Blanc JARVIS IA" width="24%" /></a>
  <a href="https://github.com/0xCyberLiTech?tab=repositories"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-github.svg" alt="Catalogue des 23 Dépôts" width="24%" /></a>
</p>
<p align="center">
  <a href="README.md"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-back-readme.svg" alt="Retour au sommaire du dépôt" width="340" /></a>
</p>

<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/divider-hud.svg" alt="" width="100%" />
</div>
<!-- MASTER-HEADER-END -->

<!-- DEBIAN-TRUTH-START -->
> [!IMPORTANT]
> <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-shield.svg" width="18" height="18" align="absmiddle" alt="" /> ** Matrice Officielle Debian — `Debian 12 (Bookworm)` · `Debian 13 (Trixie)` · `Debian 14 (Forky)`**
> - **Sources Officielles Debian.org (`openssl`) :** `Bookworm (12)` : **`3.0.20-1~deb12u2`** &nbsp;·&nbsp; `Trixie (13 — Stable)` : **`3.5.7-1~deb13u2`** &nbsp;·&nbsp; `Forky (14 — Next-Gen)` : **`3.6.5-1`**
> - **Références Officielles :** [Paquet Debian Trixie (`openssl`)](https://packages.debian.org/trixie/openssl) &nbsp;·&nbsp; [Paquet Debian Forky (`openssl`)](https://packages.debian.org/forky/openssl) &nbsp;·&nbsp; [Documentation Officielle Debian](https://manpages.debian.org/trixie/openssl/openssl.1ssl.en.html)
> - **Note d'Ingénierie (Divergence 13 vs 14) :** Debian 13 (Trixie) et Debian 14 (Forky) embarquent OpenSSL 3.x+ qui désactive par défaut les algorithmes hérités (SHA-1, RSA < 2048 bits) et introduit sous Forky les primitives post-quantiques (ML-KEM / ML-DSA).

<details>
<summary><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-doc.svg" width="18" height="18" align="absmiddle" alt="" /> <b>Afficher les Encarts Ligne de Commande : Debian 13 (Trixie — Stable) vs Debian 14 (Forky — Next-Gen)</b></summary>

#### <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-ok.svg" width="42" height="16" align="absmiddle" alt="[OK]" /> Profil Production Stable — Commandes pour `Debian 13 (Trixie)`
```bash
# Debian 13 (Trixie — OpenSSL 3.x) : Generation de cle Ed25519 & hash SHA-512
openssl genpkey -algorithm Ed25519 -out private_ed25519.pem
openssl dgst -sha512 fichier.bin
```

#### <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-rd.svg" width="46" height="16" align="absmiddle" alt="[R&D]" /> Profil Anticipation Next-Gen — Commandes pour `Debian 14 (Forky)`
```bash
# Debian 14 (Forky — OpenSSL 3.4+ Post-Quantum Ready) : Support ML-KEM / Kyber & TLS 1.3 strict
openssl list -kem-algorithms
openssl req -x509 -newkey ed25519 -days 365 -nodes -keyout key.pem -out cert.pem
```

</details>
<!-- DEBIAN-TRUTH-END -->

<!-- CIEL-PEDAGOGY-START -->
<details>
<summary><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-puzzle.svg" width="18" height="18" align="absmiddle" alt="" /> <b>Synthèse d'Architecture, Standards Officiels &amp; Diagnostic (Niveau 1 : Fondamentaux · Niveau 2 : Repères · Niveau 3 : Diagnostic)</b></summary>

- **Niveau 1 — Fondamentaux &amp; Principe d'Architecture :** La **Cryptographie Appliquée & PKI** met en œuvre les mécanismes mathématiques garantissant la **Confidentialité** (chiffrement symétrique AES-GCM / ChaCha20-Poly1305), l'**Intégrité** (hachage SHA-256 / SHA-512), l'**Authentification** (certificats X.509 / mTLS) et la **Non-répudiation** (signatures Ed25519 / RSA-PSS).
- **Niveau 2 — Repères Officiels (Ports IANA, Fichiers Debian &amp; Commandes de Validation) :** **Outils & Validation officielle :** `openssl version -a` · `openssl x509 -in cert.pem -text -noout` (Inspection X.509) · `openssl s_client -connect hote:443 -tls1_3` (Audit TLS) · `sha256sum -c fichier.sha256`.
- **Niveau 3 — Diagnostic d'Incidents &amp; Ingénierie Avancée :** **Diagnostic & Architecture :** Distinguez strictement le **Hachage** (empreinte irréversible à sens unique destinée à vérifier l'intégrité d'un fichier ou stocker un secret avec `Argon2id`) et le **Chiffrement** (transformation réversible par clé secrète ou paire de clés asymétriques). En **TLS 1.3**, l'échange de clés éphémères (`ECDHE` / `ML-KEM`) assure la confidentialité persistante (*Perfect Forward Secrecy*).
- **Sources de Vérité Officielles Éditeurs &amp; Standards :** [Documentation Officielle OpenSSL 3.x](https://docs.openssl.org/master/) &nbsp;·&nbsp; [RFC 8446 (IETF TLS 1.3)](https://datatracker.ietf.org/doc/html/rfc8446) &nbsp;·&nbsp; [Guide Cryptographique ANSSI](https://cyber.gouv.fr/)
- **Livres Blancs &amp; 67 Podcasts Audio R&amp;D :** [Portail 0xCyberLiTech](https://0xcyberlitech.com/) &nbsp;·&nbsp; [Livre Blanc SOC Cockpit v5.5](https://0xcyberlitech.com/soc-rd.html) &nbsp;·&nbsp; [Livre Blanc JARVIS Mark-VII](https://0xcyberlitech.com/jarvis-rd.html) &nbsp;·&nbsp; [Blueprint Logiciel &amp; Matériel RTX 5080](https://0xcyberlitech.com/blueprint-jarvis.html)

</details>
<!-- CIEL-PEDAGOGY-END -->


# <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-crypto.svg" width="18" height="18" align="absmiddle" alt="" /> Introduction à la Cryptographie

La **cryptographie** est la science qui permet de **protéger les informations** en les rendant illisibles pour toute personne non autorisée. Elle est au cœur de la cybersécurité moderne, utilisée dans des domaines variés comme les communications, les transactions bancaires, ou encore les systèmes de messagerie.

---

## <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-brain.svg" width="18" height="18" align="absmiddle" alt="" /> Pourquoi la cryptographie est-elle importante ?
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/glow-section-cyan.svg" width="100%" alt="" />

Imagine que vous envoyez une lettre secrète à un ami. Si quelqu’un l’intercepte, il peut lire son contenu. La cryptographie agit comme une **enveloppe blindée** : elle rend le message incompréhensible sans une **clé secrète**.

---

## <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-crypto.svg" width="18" height="18" align="absmiddle" alt="" /> Concepts clés
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/glow-section-cyan.svg" width="100%" alt="" />

- **Chiffrement** : Transformer un message clair (texte lisible) en un message codé (texte chiffré).
- **Déchiffrement** : Revenir du message codé au message original à l’aide d’une clé.
- **Clé** : Élément secret ou public permettant le chiffrement et/ou le déchiffrement.
- **Algorithme cryptographique** : Méthode utilisée pour chiffrer/déchiffrer les données (ex : AES, RSA).
- **Hachage** : Créer une empreinte unique d’un fichier ou message. Très utile pour vérifier l’intégrité.

---

## <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-puzzle.svg" width="18" height="18" align="absmiddle" alt="" /> Deux grandes familles de cryptographie
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/glow-section-cyan.svg" width="100%" alt="" />

### <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-target.svg" width="18" height="18" align="absmiddle" alt="" /> 1. Cryptographie symétrique

<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-crypto.svg" width="18" height="18" align="absmiddle" alt="" /> Une seule clé est utilisée pour chiffrer et déchiffrer. 
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-doc.svg" width="18" height="18" align="absmiddle" alt="" /> Rapide, mais nécessite un échange sécurisé de la clé.

### <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-target.svg" width="18" height="18" align="absmiddle" alt="" /> 2. Cryptographie asymétrique

<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-crypto.svg" width="18" height="18" align="absmiddle" alt="" /> Utilise une paire de clés : une **publique** (partagée) et une **privée** (secrète). 
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-doc.svg" width="18" height="18" align="absmiddle" alt="" /> Plus sécurisée pour les échanges à distance (ex : RSA).

---

## <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-shield.svg" width="18" height="18" align="absmiddle" alt="" /> Utilisations courantes
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/glow-section-cyan.svg" width="100%" alt="" />

- **Connexion HTTPS** sur les sites web
- **Messageries sécurisées** (Signal, WhatsApp)
- **Signatures numériques** pour valider l’authenticité d’un document
- **Stockage chiffré** sur vos appareils

---

## <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-doc.svg" width="18" height="18" align="absmiddle" alt="" /> Conclusion
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/glow-section-cyan.svg" width="100%" alt="" />

La cryptographie est essentielle pour garantir la **confidentialité**, **l'intégrité**, et **l'authenticité** des données. Bien qu’elle repose sur des mathématiques complexes, ses applications sont partout dans notre vie numérique.

<!-- MASTER-FOOTER-START -->
<div align="center">
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/divider-hud.svg" alt="" width="100%" />

<a href="https://0xcyberlitech.com/">
  <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/footer-master.svg" alt="0xCyberLiTech — Architecture Cyberdéfense, Ingénierie Déterministe & IA Souveraine" width="100%" />
</a>

<p align="center"><a href="https://0xcyberlitech.com/"><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/badge-antigravity.svg" alt="Architecturé par Marc & Antigravity (Google DeepMind)" width="520" /></a></p>

<sub><b>Architecturé &amp; Forgé par Marc &amp; Antigravity (Google DeepMind)</b> &nbsp;·&nbsp; <a href="https://0xcyberlitech.com/"><b>0xcyberlitech.com</b></a> &nbsp;·&nbsp; <a href="https://0xcyberlitech.com/soc-rd.html">Architecture SOC Cockpit v5.5</a> &nbsp;·&nbsp; <a href="https://0xcyberlitech.com/jarvis-rd.html">Architecture JARVIS Mark-VII</a> &nbsp;·&nbsp; <a href="https://0xcyberlitech.com/blueprint-jarvis.html">Blueprint Matériel RTX 5080</a></sub>

</div>
<!-- MASTER-FOOTER-END -->
