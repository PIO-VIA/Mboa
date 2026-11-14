# Mboa — Ta banque dans ta langue

[![SAFINUM Innovate Challenge](<https://img.shields.io/badge/CNEF-SAFINUM%20INNOVATE%20CHALLENGE%202026-0f766e?style=for-the-badge>)](https://safinum.cm)
[![Équipe GIFA](https://img.shields.io/badge/%C3%89quipe-GIFA-2563eb?style=for-the-badge)](#%C3%A9quipe-gifa)
[![Intégrité Financière](<https://img.shields.io/badge/S%C3%A9curit%C3%A9-Double%20Contrat%20BEAC%2FCOBAC-16a34a?style=for-the-badge>)](#-pipeline-de-s%C3%A9curit%C3%A9-%C3%A0-double-contrat)
[![Tests Unitaires](<https://img.shields.io/badge/Tests-21%2F21%20Valid%C3%A9s-brightgreen?style=for-the-badge>)](#-tests-et-qualit%C3%A9)
[![Mozilla Linter](<https://img.shields.io/badge/web--ext%20lint-0%20erreur%2C%200%20warning-blue?style=for-the-badge>)](#-tests-et-qualit%C3%A9)

**Mboa** est une extension web d'accessibilité linguistique universelle et de sécurité financière active conçue spécifiquement pour l'écosystème bancaire et Mobile Money camerounais.

Développée par l'**Équipe GIFA** pour le **SAFINUM INNOVATE CHALLENGE 2026**, organisé par le **Comité National Économique et Financier du Cameroun (CNEF)**, Mboa s'intègre en surcouche étanche sur **n'importe quelle application financière web** (banque en ligne, plateforme Mobile Money, microfinance) sans en modifier le code source, de manière **100 % autonome côté client (in-browser)**, gratuite, et **sans aucun serveur externe ni fuite de données privées**.

---

## 👥 Équipe GIFA

* **Nom de l'équipe** : **GIFA** (*Groupe d'Innovation pour la Finance Accessible*)
* **Compétition** : SAFINUM INNOVATE CHALLENGE 2026
* **Organisateur** : Comité National Économique et Financier du Cameroun (CNEF)

---

## 🎯 Problématique & Solution

### Le constat au Cameroun

Plus d'un citoyen camerounais sur deux éprouve des réticences ou des difficultés face au jargon bancaire complexe formulé exclusivement en français ou en anglais. Cette barrière de la langue engendre une vulnérabilité accrue aux arnaques Mobile Money récurrentes et limite l'inclusion financière des populations non francophones ou non anglophones.

### La réponse apportée par Mboa

Mboa injecte une couche d'accessibilité native et de protection active directement dans le navigateur :

1. **Compréhension immédiate** : Traduction transparente et réversible dans 4 grandes langues nationales camerounaises (**Ewondo**, **Duala**, **Fulfulde**, **Pidgin**).
2. **Double contrat d'intégrité** : Montants, numéros et références sont rigoureusement isolés ; la traduction ne voit aucun chiffre et ne peut en altérer aucun.
3. **Vérification mathématique indépendante** : L'extension recalcule les frais et totaux affichés par le service financier et alerte instantanément en cas d'erreur ou de surfacturation.
4. **Bouclier anti-fraude local** : Détection des tentatives d'escroquerie (Stop Arnaque 237) et d'usurpation d'opérateurs (MTN, Orange, banques).
5. **Accompagnement vocal et visuel** : Lecture à voix haute, récapitulatif détaillé avec billets FCFA illustrés et guidage pas à pas.

---

## 🌟 Fonctionnalités Clés

| Fonctionnalité                         | Description et Garantie                                                                                                                                                                                                                                                    |
| :-------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 🔒 **Montants verrouillés**      | Montants, frais, numéros de téléphone, IBAN/comptes, dates et références sont extraits avant traduction et réinjectés à l'identique. Tout ajout ou altération de chiffre rejette la traduction.                                                                   |
| 🧮 **Calculs vérifiés**         | Mboa vérifie de manière indépendante l'équation `Total = Montant + Frais` et le respect des barèmes réglementaires affichés.                                                                                                                                      |
| 🪞 **Contrôle Saisi = Affiché** | Les données saisies dans les formulaires sont comparées à l'écran de récapitulatif afin d'intercepter les altérations silencieuses de montant ou de bénéficiaire.                                                                                                  |
| 🛡 **Bouclier anti-arnaque**      | Moteur heuristique 100 % local entraîné sur le corpus réel *Stop Arnaque 237* : alerte sur les demandes de code secret/PIN, faux transferts par erreur, pressions d'urgence et faux sites bancaires. **0 fausse alerte sur 180 messages officiels vérifiés**. |
| 🌐 **Détection automatique**     | Détection automatique du français et de l'anglais. Traduction fluide de la page active et des navigations SPA dynamiques (MutationObserver).                                                                                                                             |
| 🧾 **Récapitulatif FCFA**        | Fiche claire « Avant de confirmer » avec décomposition schématique en billets et pièces BEAC (10 000, 5 000, 2 000, 1 000 FCFA).                                                                                                                                      |
| 🔊 **Voix & Synthèse**           | Écoute de la page, du récapitulatif et des alertes. Prise en charge des enregistrements audio de locuteurs natifs validés dans le Studio.                                                                                                                               |
| 🧩 **Composition par Blocs**      | Assemblage hors ligne de phrases financières inédites à partir de 56 blocs syntaxiques relus, sans appel LLM risquant d'inventer des chiffres.                                                                                                                          |
| 🔎 **Diagnostic de transparence** | Si un terme est inconnu, Mboa conserve l'original intact, affiche l'intention générale et surligne les mots manquants via l'API standard *CSS Custom Highlight*.                                                                                                       |
| 🎙 **Studio Linguistique**        | Espace intégré (`studio/studio.html`) permettant aux linguistes et locuteurs natifs de relire, corriger, valider (double signature) et enregistrer leur voix.                                                                                                          |

---

## 🌍 Langues Nationales Prises en Charge

Mboa couvre les principales zones géolinguistiques du Cameroun :

| Langue                                  | Code ISO          | Régions couvertes                                     | Statut linguistique |
| :-------------------------------------- | :---------------- | :----------------------------------------------------- | :------------------ |
| **Ewondo**                        | `ewo`           | Centre, Sud (Yaoundé et ses environs)                 | Relu et validé     |
| **Duálá**                       | `dua`           | Littoral (Douala, bassin du Wouri)                     | Relu et validé     |
| **Fulfulde**                      | `fub`           | Adamaoua, Nord, Extrême-Nord                          | Relu et validé     |
| **Pidgin (Kamtok)**               | `wes` / `pcm` | Nord-Ouest, Sud-Ouest, Littoral, véhiculaire national | Relu et validé     |
| **Français** / **Anglais** | `fr` / `en`   | Langues officielles de source                          | Langues sources     |

### Protocole de validation linguistique

* **Double relecture native indépendante** : Une phrase n'obtient le statut `validated` qu'après validation concordante de deux locuteurs natifs distincts.
* **Rétro-traduction orale à l'aveugle** : Contrôle par un troisième locuteur pour s'assurer de l'absence de contresens financier.
* **Garde-fous cryptographiques et structurels** : Le Studio refuse tout enregistrement ou export de pack qui omet une variable `{0}` ou injecte un chiffre absent du texte original.

---

## 🏗 Architecture Technique

L'extension fonctionne entièrement côté client selon une architecture en couches étanches :

```
[PAGE BANCAIRE DISTANTE] (Code 100% inchangé) | DOM initial + Détection SPA (MutationObserver)
  │
  ▼
[DOM Walker & Scanner] (mboa/src/content/dom.js)
  │  Collecte ciblée des nœuds texte (hors balises sensibles et scripts)
  ▼
[Moteur de Traduction Sécurisé] (mboa/src/core/engine.js)
  ├─ 1. entities.protect()  : Extraction regex des montants, %, téléphones, comptes, dates
  ├─ 2. Mémoire d'Intentions : Dictionnaire validé sur phrases bancaires canoniques (FR / EN)
  ├─ 3. Composition Blocs   : Assemblage syntaxique hors ligne de phrases inédites
  ├─ 4. Mode Sauvegarde     : Si non reconnu, annonce de l'intention + texte original préservé
  └─ 5. entities.verify()   : Double contrat d'intégrité (restitution intégrale des jetons)
  │
  ▼
[Couche d'Application DOM]
  │  Écriture en place exclusive via nodeValue (texte original conservé en mémoire)
  ▼
[Moteurs Financiers & Sécurité] (mboa/src/content/main.js)
  ├─ money.extractFacts()   : Lecture sémantique des montants, frais et totaux
  ├─ money.checks()         : Recalcul mathématique (Total = Montant + Frais ; barème opérateur)
  ├─ shield.scoreText()     : Détection locale d'arnaques (schémas réels Stop Arnaque 237)
  └─ ui.js (Shadow DOM)     : Injection étanche du panneau de contrôle, récapitulatif FCFA et voix
```

---

## 📁 Structure du Répertoire

```
linguafin/
├── README.md                      # Documentation principale du projet (Équipe GIFA)
├── package.json                   # Définition du projet et commandes npm
├── scripts/
│   ├── build.mjs                  # Script automatisé de compilation et d'empaquetage
│   └── generate_dossier_pdf.mjs   # Générateur du dossier technique officiel SAFINUM GIFA (PDF)
├── mboa/                          # Code source de l'extension universelle
│   ├── manifest.json              # Manifeste WebExtension MV3 universel
│   ├── icons/                     # Icônes de l'extension (16, 32, 48, 128 px)
│   ├── popup/                     # Popup de configuration rapide
│   ├── studio/                    # Studio linguistique de validation et d'enregistrement audio
│   ├── validation/                # Feuilles de validation CSV officielles par langue
│   │   ├── GUIDE_VALIDATEURS.md   # Guide méthodologique pour les validateurs natifs
│   │   ├── mboa-validation-ewo.csv
│   │   ├── mboa-validation-dua.csv
│   │   ├── mboa-validation-fub.csv
│   │   └── mboa-validation-pcm.csv
│   ├── src/
│   │   ├── background.js          # Service worker / script d'arrière-plan minimal
│   │   ├── core/                  # Moteurs d'analyse et de sécurité
│   │   │   ├── ns.js              # Initialisation de l'espace de noms MBOA
│   │   │   ├── detect.js          # Détecteur heuristique de langue source (FR / EN)
│   │   │   ├── entities.js        # Verrouillage d'entités sensibles et contrat d'intégrité
│   │   │   ├── engine.js          # Moteur de traduction par intentions et composition
│   │   │   ├── money.js           # Moteur financier, vérifications et devises BEAC
│   │   │   ├── shield.js          # Bouclier heuristique anti-fraude (Stop Arnaque 237)
│   │   │   └── icons.js           # Bibliothèque d'icônes vectorielles SVG intégrées
│   │   ├── packs/                 # Données linguistiques validées
│   │   │   ├── phrases.js         # Mémoire de phrases financières validées
│   │   │   └── blocks.js          # Blocs syntaxiques pour la composition hors ligne
│   │   └── content/               # Scripts de contenu injectés
│   │       ├── dom.js             # Manipulation DOM réversible et surlignage CSS Highlight
│   │       ├── voice.js           # Gestionnaire vocal (synthèse Web Speech et audio natif)
│   │       ├── ui.js              # Interface Shadow DOM isolée (bouton, panneau, récapitulatif)
│   │       └── main.js            # Chef d'orchestre principal et raccourcis clavier
│   └── docs/
│       ├── NOTE_TECHNIQUE.md      # Note technique détaillée
│       └── captures/              # Captures d'écran officielles de l'interface
└── dist/                          # Paquets compilés prêts à l'emploi (générés par npm run build)
    ├── chrome/                    # Version décompressée pour Chromium / Edge / Brave
    ├── firefox/                   # Version décompressée pour Mozilla Firefox
    ├── mboa/                      # Version universelle
    ├── mboa-chrome.zip            # Archive distribuable Chrome Web Store
    ├── mboa-firefox.zip           # Archive distribuable Mozilla Add-ons
    └── mboa-universel.zip         # Archive universelle
```

---

## 🔨 Guide de Compilation, Installation & Lancement Pas à Pas

Suivez ces étapes simples pour compiler le projet à partir des sources, générer les paquets optimisés pour chaque navigateur et lancer l'extension en test.

### 1. Prérequis
* **Node.js** : Version 18.0 ou supérieure (`node -v`).
* **npm** : Gestionnaire de paquets standard fourni avec Node (`npm -v`).
* Un navigateur moderne : **Google Chrome**, **Mozilla Firefox**, **Brave**, **Microsoft Edge**, ou **Firefox pour Android**.

### 2. Étape 1 : Installation des dépendances
À la racine du projet (`linguafin/`), installez les outils de test et de validation :
```bash
npm install
```

### 3. Étape 2 : Vérification des tests unitaires de sécurité
Avant toute compilation, lancez la suite complète de 21 tests unitaires validant l'intégrité financière, le bouclier anti-fraude et la composition syntaxique :
```bash
npm test
```
> **Résultat attendu** : `pass 21 / fail 0` (100 % de réussite).

### 4. Étape 3 : Compilation et génération des paquets (`npm run build`)
Exécutez le script automatisé de compilation :
```bash
npm run build
```
Ce script exécute automatiquement :
1. Les 21 tests unitaires de sécurité.
2. Le nettoyage et la préparation du répertoire de distribution `dist/`.
3. La génération des déclinaisons de manifestes conformes aux exigences strictes de chaque moteur de navigateur (Manifest V3 avec `service_worker` pour Chromium, Manifest V3 avec `scripts` d'arrière-plan pour Firefox).
4. La validation officielle par le linter Mozilla (`web-ext lint` : **0 erreur, 0 avertissement**).
5. La compression automatique des archives ZIP prêtes au déploiement.

**Livrables générés dans `dist/` :**
* `dist/chrome/` & `dist/mboa-chrome.zip` : Pour Google Chrome, Edge, Brave, Opera.
* `dist/firefox/` & `dist/mboa-firefox.zip` : Pour Mozilla Firefox et Firefox pour Android.
* `dist/mboa/` & `dist/mboa-universel.zip` : Paquet universel multi-navigateurs.

---

### 5. Étape 4 : Charger l'extension dans votre navigateur

#### Pour Google Chrome, Microsoft Edge, Brave ou Opera :
1. Ouvrez votre navigateur et saisissez l'adresse : `chrome://extensions` (ou `edge://extensions`).
2. Activez le commutateur **« Mode développeur »** (en haut à droite de la page).
3. Cliquez sur le bouton **« Charger l'extension non empaquetée »** (*Load unpacked*).
4. Sélectionnez le dossier compilé **`dist/chrome/`** (ou directement le dossier source `mboa/`).
5. L'extension **Mboa** apparaît immédiatement dans la liste de vos extensions !
6. *(Recommandé)* Cliquez sur l'icône Puzzle en haut à droite de la barre d'outils et **épinglez Mboa** pour un accès rapide.

#### Pour Mozilla Firefox ou Firefox pour Android :
1. Ouvrez Firefox et accédez à : `about:debugging#/runtime/this-firefox`.
2. Cliquez sur le bouton **« Charger un module temporaire... »** (*Load Temporary Add-on*).
3. Naviguez dans le dossier et sélectionnez le fichier **`dist/firefox/manifest.json`** (ou `mboa/manifest.json`).
4. L'extension est activée avec 0 avertissement de compatibilité.

---

### 6. Étape 5 : Lancer la démo et tester les fonctionnalités

Une fois l'extension chargée, testez-la immédiatement sur l'un des environnements suivants :

#### Option A : Plateforme officielle du hackathon CNEF (En ligne)
1. Rendez-vous sur la plateforme officielle : **[https://safinum.cm/hackathon-test?jury=1](https://safinum.cm/hackathon-test?jury=1)**
2. La pastille flottante **M** apparaît immédiatement en bas à gauche de la page bancaire.
3. **Changer de langue** : Cliquez sur la pastille et choisissez une langue (ex. **Ewondo**, **Duala**, **Fulfulde** ou **Pidgin**). L'interface bascule instantanément sans recharger la page.
4. **Vérifier les calculs et devises FCFA** : Naviguez jusqu'à l'étape des Frais. La carte flottante *« Avant de confirmer »* s'ouvre, ventilant le montant en billets FCFA réels de la BEAC et vérifiant l'exactitude des frais.
5. **Vérification du Jury** : Cliquez sur le bouton *« Vérifier l'étape maintenant »* de la bannière jury : le journal confirme que tous les montants et identifiants restent **Intègres**.

#### Option B : Simulateur bancaire hors ligne inclus (100 % local)
Si vous n'avez pas de connexion Internet, ouvrez simplement le fichier de démonstration locale fourni :
```bash
# Exemple sous Linux / macOS :
xdg-open mboa-demo/index.html
# Ou glissez simplement mboa-demo/index.html dans votre navigateur
```
Ce simulateur bancaire (*Kola Pay*) permet de tester le transfert, le barème de frais, les simulations d'erreur et les alertes anti-arnaque de manière autonome.

---

### 7. Étape 6 : Accéder au Studio Linguistique Mboa
Pour inspecter la mémoire de phrases, valider de nouveaux termes ou enregistrer des voix natives :
* Cliquez sur le lien **« Studio linguistique »** dans le pied du panneau Mboa ou dans le popup.
* Ou ouvrez directement dans votre navigateur : `dist/chrome/studio/studio.html` (ou `mboa/studio/studio.html`).
* Les validateurs natifs peuvent y importer des feuilles de validation CSV, filtrer les statuts et écouter les enregistrements audio.

---

## 🛠 Commandes & Scripts Utiles

Toutes les tâches de cycle de vie du projet sont automatisées via npm :

```bash
# 1. Exécuter la suite complète de 21 tests unitaires de sécurité
npm test

# 2. Compiler l'ensemble des paquets et archives de distribution
npm run build

# 3. Contrôler la conformité officielle Mozilla (web-ext lint)
npm run lint:firefox

# 4. Générer le Dossier Technique officiel SAFINUM GIFA au format PDF
npm run dossier:pdf

# 5. Lancer l'évaluation du bouclier anti-arnaque sur données réelles
npm run shield
```

---

## ⌨️ Raccourcis Clavier

Pour une accessibilité maximale au clavier :

* <kbd>Alt</kbd> + <kbd>Maj</kbd> + <kbd>M</kbd> : Ouvrir ou fermer le panneau de contrôle Mboa.
* <kbd>Alt</kbd> + <kbd>Maj</kbd> + <kbd>L</kbd> : Démarrer la lecture à voix haute de la page.
* <kbd>Alt</kbd> + <kbd>Maj</kbd> + <kbd>O</kbd> : Basculer instantanément entre la langue nationale et le texte original.
* <kbd>Alt</kbd> + <kbd>Maj</kbd> + <kbd>S</kbd> : Arrêter immédiatement la voix de synthèse.
* <kbd>Alt</kbd> + Clic sur un texte traduit : Écouter la prononciation du segment cliqué.

---

## 📄 Licence & Crédits

* **Projet** : Mboa — Développé par l'**Équipe GIFA** pour le **SAFINUM INNOVATE CHALLENGE 2026** (CNEF Cameroun).
* **Données de test anti-fraude** : Dataset public [*Stop Arnaque 237*](https://huggingface.co/datasets/kadian-arch/stop-arnaque-237) (Licence Creative Commons CC BY 4.0).
* **Icônes** : Tracés vectoriels SVG inspirés des catalogues ouverts Lucide (ISC) et Heroicons (MIT).
* **Respect de la vie privée** : Déclaration formelle `data_collection_permissions: none`. Aucune donnée collectée, aucun cookie déposé, aucun appel réseau sortant.
