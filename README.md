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
> [!TIP]
> <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-target.svg" width="18" height="18" align="absmiddle" alt="" /> **Guide de Lecture &amp; Progression par Niveau (Cryptographie)**
> - **Rôle de la brique :** La **Cryptographie Appliquée & PKI** met en œuvre les mécanismes mathématiques garantissant la **Confidentialité** (chiffrement symétrique AES-GCM / ChaCha20-Poly1305), l'**Intégrité** (hachage SHA-256 / SHA-512), l'**Authentification** (certificats X.509 / mTLS) et la **Non-répudiation** (signatures Ed25519 / RSA-PSS).
> - **Parcours recommandé :** **Niveau 1 (Fondamentaux &amp; Installation initiale)** pour déployer une base saine &rarr; **Niveau 2 (Configuration &amp; Intégration)** &rarr; **Niveau 3 (Haute Disponibilité, Durcissement &amp; Exploitation)**.

<details>
<summary><img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-puzzle.svg" width="18" height="18" align="absmiddle" alt="" /> <b>Synthèse d'Architecture, Standards Officiels &amp; Diagnostic (Niveau 1 : Fondamentaux · Niveau 2 : Repères · Niveau 3 : Diagnostic)</b></summary>

- **Niveau 1 — Fondamentaux &amp; Principe d'Architecture :** La **Cryptographie Appliquée & PKI** met en œuvre les mécanismes mathématiques garantissant la **Confidentialité** (chiffrement symétrique AES-GCM / ChaCha20-Poly1305), l'**Intégrité** (hachage SHA-256 / SHA-512), l'**Authentification** (certificats X.509 / mTLS) et la **Non-répudiation** (signatures Ed25519 / RSA-PSS).
- **Niveau 2 — Repères Officiels (Ports IANA, Fichiers Debian &amp; Commandes de Validation) :** **Outils & Validation officielle :** `openssl version -a` · `openssl x509 -in cert.pem -text -noout` (Inspection X.509) · `openssl s_client -connect hote:443 -tls1_3` (Audit TLS) · `sha256sum -c fichier.sha256`.
- **Niveau 3 — Diagnostic d'Incidents &amp; Ingénierie Avancée :** **Diagnostic & Architecture :** Distinguez strictement le **Hachage** (empreinte irréversible à sens unique destinée à vérifier l'intégrité d'un fichier ou stocker un secret avec `Argon2id`) et le **Chiffrement** (transformation réversible par clé secrète ou paire de clés asymétriques). En **TLS 1.3**, l'échange de clés éphémères (`ECDHE` / `ML-KEM`) assure la confidentialité persistante (*Perfect Forward Secrecy*).
- **Sources de Vérité Officielles Éditeurs &amp; Standards :** [Documentation Officielle OpenSSL 3.x](https://docs.openssl.org/master/) &nbsp;·&nbsp; [RFC 8446 (IETF TLS 1.3)](https://datatracker.ietf.org/doc/html/rfc8446) &nbsp;·&nbsp; [Guide Cryptographique ANSSI](https://cyber.gouv.fr/)

</details>
<!-- CIEL-PEDAGOGY-END -->


## <img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/icons/wire-plan.svg" width="18" height="18" align="absmiddle" alt="" /> 01 // SOMMAIRE DES DOSSIERS TECHNIQUES — ATELIER CRYPTOGRAPHIE // PKI & TLS
<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/glow-section-cyan.svg" width="100%" alt="" />

<div align="center">

| Catégorie         | Description   | Accès Rapide                                                                                                                                                                                              |
|-------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Cryptographie** | Introduction. | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](CYBERSECURITE-CRYPTOGRAPHIE-introduction.md)                                                   |
| **Cryptographie** | Cours.        | [<img src="https://raw.githubusercontent.com/0xCyberLiTech/0xcyberlitech/main/assets/btn-explore.svg" alt="Ouvrir le dossier" />](https://github.com/0xCyberLiTech/CRYPTOGRAPHIE/blob/main/CYBERSECURITE-CRYPTOGRAPHIE-COURS.md) |

</div>

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
