<div align="center">

<img src="android/app/src/main/res/drawable-nodpi/logo.png" width="110" alt="Logo Upscayl">

# Upscayl Mobile

**Portage mobile non officiel d'Upscayl pour iOS et Android**

Agrandis et améliore tes images avec l'IA, directement sur ton téléphone.

[![Android](https://img.shields.io/badge/Android-T%C3%A9l%C3%A9charger_l'APK-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://github.com/akuuvfx/upscayl-ios/releases/download/latest/Upscayl-Android.apk)
[![iOS](https://img.shields.io/badge/iOS-T%C3%A9l%C3%A9charger_l'IPA-111111?style=for-the-badge&logo=apple&logoColor=white)](https://github.com/akuuvfx/upscayl-ios/releases/download/latest/Upscayl.ipa)

</div>

---

> **Projet non officiel.** Ce dépôt n'est ni affilié, ni approuvé, ni soutenu par l'équipe Upscayl.
> « Upscayl », son nom et son logo appartiennent à leurs auteurs. Ils sont utilisés ici uniquement
> pour décrire la compatibilité et l'origine des modèles. Voir [Nature du portage](#nature-du-portage).

## :arrow_down: Téléchargement

Les liens ci-dessous pointent toujours vers **la dernière version** : ils ne changent jamais.

| Plateforme | Lien direct | Configuration |
|---|---|---|
| :robot: **Android** | [Upscayl-Android.apk](https://github.com/akuuvfx/upscayl-ios/releases/download/latest/Upscayl-Android.apk) | Android 10 ou plus, processeur 64 bits |
| :apple: **iOS** | [Upscayl.ipa](https://github.com/akuuvfx/upscayl-ios/releases/download/latest/Upscayl.ipa) | iOS 16 ou plus |

### Installation

**Android**
1. Ouvre le lien sur ton téléphone et télécharge l'APK.
2. Autorise l'installation depuis cette source si Android le demande.
3. Ouvre le fichier et installe.

**iOS** : le fichier n'est pas signé, il s'installe par sideloading depuis un ordinateur avec [Sideloadly](https://sideloadly.io) ou [AltStore](https://altstore.io).

---

## :sparkles: Fonctionnalités

- Agrandissement de **×1 à ×16** : l'IA travaille en ×4, puis l'image est redimensionnée.
  **Double Upscayl** enchaîne deux passes d'IA pour un meilleur résultat (jusqu'à ×16).
- **7 modèles** d'IA : Standard, Lite, High Fidelity, Digital Art, Remacri, Ultramix, Ultrasharp.
- **Traitement par lot** : jusqu'à 30 images, avec navigation, progression et réessai.
- **Calcul en arrière-plan** sur iOS 26 (tâche de traitement continu) et **notification de fin**.
- **Comparaison avant / après** avec curseur, zoom au pincement et déplacement.
- Réglages avancés : unité de calcul (CPU / GPU / Neural Engine), taille de tuile, **TTA**,
  largeur de sortie personnalisée, compression, format **PNG / JPG / HEIC**.
- **Tout est traité localement** : aucune image n'est envoyée sur un serveur.
- Interface en verre translucide, thèmes de couleur, apparence claire / sombre.
- Application en **français** ou en **anglais** (réglage dans l'onglet « Paramètres »).
- Vérification des mises à jour depuis GitHub.

---

## Nature du portage

Ce dépôt n'est **pas un fork du code desktop d'Upscayl**. C'est une **adaptation mobile
indépendante**, écrite spécifiquement pour iOS et Android. Le mot « portage » est utilisé au sens
large : même famille de modèles et même objectif, mais pas un portage ligne à ligne de
l'application Electron/JavaScript d'origine.

| Élément | Origine |
|---|---|
| **Modèles d'IA** (`.param` / `.bin` ncnn → `.mlmodelc` Core ML) | Modèles publiés dans le dépôt Upscayl, eux-mêmes dérivés de Real-ESRGAN et d'autres auteurs. Chaque modèle garde sa licence d'origine. |
| **Code iOS** (`Sources/`) | Écrit pour ce projet : Swift, SwiftUI, Core ML, Core Image, BackgroundTasks. |
| **Code Android** (`android/`) | Écrit pour ce projet : Kotlin, Jetpack Compose, ncnn (Vulkan, repli CPU). |
| **Interface, comparaison, lot, réglages** | Conçus pour ce projet, inspirés de l'ergonomie d'Upscayl. |
| **Nom « Upscayl », logo, captures** | Propriété de leurs auteurs. Utilisés de façon descriptive, sans revendication de marque. |

**Ce qui a été adapté pour le mobile :** conversion des modèles ncnn en Core ML, découpage en
tuiles avec recouvrement, TTA, Double Upscayl, traitement par lot, calcul en arrière-plan iOS 26,
interface tactile, thèmes, localisation FR/EN, vérification des mises à jour.

**Ce qui n'est pas inclus :** le code Electron/JavaScript d'Upscayl, son installeur, son interface
desktop et ses binaires ncnn précompilés. Le code mobile de ce dépôt est original.

**Aucune affiliation.** Ce projet n'est ni approuvé, ni parrainé, ni maintenu par l'équipe Upscayl.
Si les ayants droit demandent le retrait du nom ou du logo, ils seront remplacés sans délai.

---

## :warning: Crédits et avertissement

Ce projet est un **portage mobile non officiel d'Upscayl**, réalisé indépendamment de l'équipe originale.

L'ensemble des droits, du travail original, des marques et des ressources appartient à leurs créateurs et ayants droit respectifs. Tous les crédits reviennent aux développeurs et contributeurs originaux d'Upscayl.

Ce projet **n'est ni affilié, ni approuvé, ni soutenu officiellement par l'équipe d'Upscayl**.

Ce portage est un projet communautaire indépendant. Nous ne revendiquons aucun droit sur le projet original : tout le mérite revient aux personnes qui l'ont créé et développé.

:link: **Projet officiel :** https://github.com/upscayl/upscayl

Merci aux développeurs originaux pour leur travail !

---

## :page_facing_up: Licences

- Upscayl : AGPL-3.0 (voir [`LICENSE`](LICENSE))
- Real-ESRGAN : BSD-3-Clause (voir [`Real-ESRGAN_LICENSE.txt`](Real-ESRGAN_LICENSE.txt))
- ncnn : BSD-3-Clause
- Certains modèles (Remacri, Ultramix, Ultrasharp) sont marqués **non commercial** par leurs auteurs.
  L'application est distribuée gratuitement, sans publicité ni vente. Vérifie la licence de chaque
  modèle avant toute utilisation commerciale.

Le code de ce dépôt est distribué sous AGPL-3.0. Le code source correspondant est disponible
ici même, à la racine du dépôt. Les modifications apportées au projet d'origine sont décrites
dans la section [Nature du portage](#nature-du-portage) et dans [`CHANGELOG.md`](CHANGELOG.md).

Portage réalisé par **Akuu**, qui ne détient aucun droit sur le projet original.

---

## :rocket: Feuille de route

Améliorations prévues, classées par priorité. Les éléments déjà livrés sont marqués ✅.

### Fiabilité et mémoire
- ✅ Décodage borné en mémoire via ImageIO (évite de charger une photo 48 Mpx en pleine résolution).
- ⬜ Limite de mémoire adaptative selon l'appareil (`os_proc_available_memory`).
- ⬜ Avertissement avant un lot trop lourd (taille de sortie estimée, thermique, batterie).
- ⬜ Reprise d'un lot interrompu et nettoyage automatique des fichiers temporaires.

### Expérience utilisateur
- ✅ Progression de la phase « Préparation » (lecture iCloud, écriture des fichiers temporaires).
- ✅ Bouton « Ouvrir les Réglages » quand l'accès à Photos est refusé.
- ✅ Date de création conservée à l'enregistrement dans Photos.
- ⬜ Historique / galerie persistant des images agrandies.
- ⬜ Grille de lot avec état par image, ajout d'images, suppression et réessai.
- ⬜ Presets (« Photo », « Anime », « Texte », « Vieille photo ») et aperçu par modèle.
- ⬜ Relancer une image avec un autre modèle depuis l'écran de résultat.
- ⬜ Live Activity / Dynamic Island pour la progression.

### Entrées et sorties
- ⬜ Extension de partage iOS (« Agrandir avec Upscayl » depuis Photos, Safari, Fichiers).
- ⬜ App Intents / Shortcuts et import par glisser-déposer.
- ⬜ « Ouvrir dans Upscayl » depuis Fichiers et copie dans le presse-papiers.
- ⬜ Téléchargement des modèles à la demande (l'IPA embarque actuellement les 7 modèles).
- ⬜ Import de modèles Core ML personnalisés.

### Qualité et performance
- ✅ Notifications visibles même quand l'app est au premier plan.
- ⬜ Préservation des métadonnées EXIF et de l'espace colorimétrique Display P3.
- ⬜ Export PNG avec alpha et choix du fond pour les images transparentes.
- ⬜ Boucles pixel par pixel accélérées avec vImage / Accelerate.
- ⬜ Taille de tuile automatique selon l'appareil, préchargement du modèle.

### Accessibilité et localisation
- ⬜ VoiceOver, Dynamic Type, « Réduire les animations » et « Réduire la transparence ».
- ⬜ String Catalogs (`.xcstrings`) et langues supplémentaires.
- ⬜ Pluriels corrects, formatage localisé des nombres et support RTL.

### Qualité logicielle
- ✅ Version unique (`MARKETING_VERSION` dans `project.yml`, lue depuis le bundle).
- ✅ Manifeste de confidentialité (`PrivacyInfo.xcprivacy`).
- ⬜ Tests unitaires (tuiles, TTA, version, préférences) et tests d'image de référence.
- ✅ Build sur chaque pull request et publication uniquement depuis `main`.
- ⬜ Conversion des modèles reproductible (commit Upscayl épinglé + checksums).

---

<details>
<summary>Pour les développeurs</summary>

| Plateforme | Dossier | Moteur | Workflow |
|---|---|---|---|
| iOS | racine (`Sources/`, `project.yml`) | modèles Upscayl (ncnn) convertis en Core ML | `build-ipa.yml` |
| Android | `android/` | modèles ncnn d'Upscayl (Vulkan, repli CPU) | `build-apk.yml` |

- La version de l'app est définie **une seule fois** : `MARKETING_VERSION` dans [`project.yml`](project.yml).
  `AppInfo.version` lit `CFBundleShortVersionString` depuis le bundle.
- Les builds iOS tournent sur `push` vers `main`, sur `pull_request` et manuellement.
  La publication de la release `latest` n'a lieu que depuis `main`.
- Le manifeste de confidentialité se trouve dans `Sources/PrivacyInfo.xcprivacy`.

Chaque `git push` sur `main` lance le build correspondant sur GitHub Actions et remplace le fichier
de la release `latest`.

</details>
