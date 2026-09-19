# 🦈 Vigie Requins — La Réunion

> Tableau de bord interactif de surveillance et d'analyse du risque requin à La Réunion.
> Outil tiers indépendant — **non gouvernemental**, non affilié au CSR, à l'État français ou à l'association Ressac.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML-5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/fr/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/fr/docs/Web/JavaScript)
[![Leaflet](https://img.shields.io/badge/Leaflet-1.9.4-199900?logo=leaflet&logoColor=white)](https://leafletjs.com/)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.4.1-FF6384?logo=chart.js&logoColor=white)](https://www.chartjs.org/)

---

## 📋 Table des matières

- [Présentation](#-présentation)
- [Fonctionnalités](#-fonctionnalités)
- [Aperçu des modules](#-aperçu-des-modules)
- [Sources de données](#-sources-de-données)
- [Installation](#-installation)
- [Utilisation](#-utilisation)
- [Structure du projet](#-structure-du-projet)
- [Stack technique](#-stack-technique)
- [Limites et avertissements](#-limites-et-avertissements)
- [Feuille de route](#-feuille-de-route)
- [Contribuer](#-contribuer)
- [Licence](#-licence)
- [Remerciements](#-remerciements)

---

## 🎯 Présentation

**Vigie Requins — La Réunion** est un tableau de bord open source qui compile, visualise et analyse les **données publiques** relatives au risque requin sur l'île de La Réunion.

L'objectif est de fournir un outil de **vulgarisation et d'analyse** accessible à tous : chercheurs, journalistes, décideurs publics, associations environnementales, et grand public.

Ce projet **ne remplace pas** les dispositifs officiels de surveillance (CSR, BSAN, RESSAC) et **ne fournit pas** d'alertes en temps réel à valeur réglementaire.

### Ce que ce projet fait

- ✅ Agrège des données historiques publiques (attaques, captures, ZONEX)
- ✅ Cartographie interactive des zones à risque et des équipements
- ✅ Visualise les tendances (décennies, activités, horaires, gravité)
- ✅ Présente un panneau transparence sur les controverses documentées
- ✅ Exporte les données en CSV et PDF

### Ce que ce projet ne fait pas

- ❌ Fournir des alertes en temps réel officielles
- ❌ Accéder aux flux des vigies, drones ou BSAN
- ❌ Remplacer l'application Dorsal ou les communications du CSR
- ❌ Constituer un avis médical, juridique ou de sécurité

---

## ✨ Fonctionnalités

### 📊 Vue d'ensemble

- **8 indicateurs clés** : attaques recensées, taux de mortalité, zone la plus touchée, captures ciblées, années sans attaque, heures de pêche, taux de survie des captures accessoires, ZONEX actives.
- **Bouton d'accès direct à Dorsal** (plateforme officielle de signalement du CSR).

### 🗺️ Carte interactive (Leaflet)

**5 couches activables :**

- Attaques historiques (couleur = gravité : rouge/orange/vert)
- Heatmap de densité des attaques
- Équipements de surveillance (VRR, smart-drumlines, PHF, BRUVS, stations acoustiques, sonar, barrière)
- Spots de surf et zones à risque
- ZONEX (zones d'expérimentation)

**Autres fonctionnalités :**

- Popups détaillées au clic sur chaque point
- Légende complète en bas à droite

### 📈 Graphiques (Chart.js)

- Attaques par décennie (1980–2022)
- Répartition par activité (surf, bodyboard, plongée, pêche sous-marine)
- Répartition horaire (matin, après-midi, crépuscule, nuit)
- Captures annuelles de requins tigres et bouledogues (2014–2023)
- Gravité des attaques (léger, grave, fatal)
- Composition des captures (ciblées vs accessoires)
- Espèces protégées impactées

### 🔍 Filtres interactifs

- **Période** (décennie)
- **Gravité** (fatal, grave, léger)
- **Activité** (surf, bodyboard, plongée, pêche sous-marine)
- Mise à jour en temps réel de la carte, des tableaux et des graphiques

### 📋 Tableaux de données

- **Attaques historiques** : 48 entrées triables, recherchables, avec modale de détail
- **Captures préventives** : 548 captures ciblées + 63 accessoires
- **Zones réglementées** : ZONEX, lagons sécurisés, filets anti-requins

### 🔬 Technologies documentées

- Drones aquatiques (Cyberjet 250)
- Sonar Seapix (IXblue)
- Barrière Sharksafe (SSB®)
- Marquage acoustique (CHARC)
- Caméras BRUVS (ReMaCAP)

### ⚖️ Panneau transparence

- Taux de capture ciblée (32 %)
- Proportion de juvéniles et femelles
- Espèces protégées capturées accidentellement
- Controverse sur la publication des données (contentieux 2026)
- Débat scientifique sur l'efficacité des PAVAC

### 📤 Export

- **CSV** : attaques, captures, espèces protégées, ZONEX
- **PDF** : rapport structuré avec en-tête, résumé et tableaux

---

## 🧩 Aperçu des modules

| Module | Description |
|---|---|
| **Vue d'ensemble** | KPI, accès Dorsal, état des sources |
| **Carte interactive** | 5 couches, filtres, popups |
| **Attaques** | Tableau détaillé 1980–2022 |
| **Pêche préventive** | Captures ciblées et accessoires |
| **Technologies** | Drones, sonar, barrière, acoustique, BRUVS |
| **Zonage** | ZONEX, lagons, filets anti-requins |
| **Transparence** | Controverses et limites documentées |

---

## 📚 Sources de données

Toutes les données utilisées sont **publiques** et proviennent des sources suivantes :

### Attaques historiques

- **Centre Sécurité Requin (CSR)** — rapports officiels 1980–2022
- **Études académiques** — 46 attaques documentées (1980–2014)
- **Publications IUCN 2024** — données de captures

### Pêche préventive

- **Programme Réunionnais de Pêche de Prévention (PR2P)** — 2011–2024
- **Centre Sécurité Requin** — rapports mensuels
- **IUCN 2024** — composition des captures

### Technologies et recherche

- **Programme CHARC** — marquage acoustique (IRD)
- **Projet ReMaCAP** — caméras BRUVS (Shark Citizen / OFB)
- **Programme IRRAE** — ADN environnemental (2021–2023)
- **Projet MAEO** — réseau éco-participatif (ARBRE)
- **Observatoire Marin (Omar)** — Atlas des espèces marines

### Signalements collaboratifs

- **Dorsal** — application officielle du CSR (250 000+ utilisateurs)

### Zonage réglementaire

- **Arrêté préfectoral du 8 février 2017**
- **Centre Sécurité Requin** — ZONEX et zones aménagées

---

## 🚀 Installation

### Prérequis

Aucun. Le projet est un **fichier HTML unique** (HTML + CSS + JS inline).

### Méthode 1 — Ouverture directe

1. Téléchargez le fichier `index.html`
2. Ouvrez-le dans un navigateur moderne (Chrome, Firefox, Safari, Edge)

### Méthode 2 — Serveur local

```bash
# Avec Python
python3 -m http.server 8000

# Avec Node.js
npx serve

# Puis ouvrir http://localhost:8000/index.html
```

### Méthode 3 — Déploiement GitHub Pages

1. Créez un dépôt GitHub
2. Poussez le fichier `index.html`
3. Activez GitHub Pages dans **Settings → Pages**
4. Le site sera disponible à `https://<votre-utilisateur>.github.io/<votre-depot>/`

---

## 🖥️ Utilisation

### Navigation

- **Onglets en haut** : Vue d'ensemble, Carte, Attaques, Pêche, Technologies, Zonage, Transparence
- **Filtres** : sélectionnez une période, une gravité ou une activité
- **Carte** : activez/désactivez les couches via les boutons
- **Tableaux** : cliquez sur les en-têtes pour trier, sur une ligne pour ouvrir le détail

### Export

- **CSV** : bouton en haut à droite → fichier `.csv` (UTF-8 BOM, compatible Excel)
- **PDF** : bouton en haut à droite → rapport structuré A4

### Raccourcis clavier

| Touche | Action |
|---|---|
| `Échap` | Fermer la modale |
| `Clic` sur ligne | Ouvrir le détail |

---

## 📁 Structure du projet

```
vigie-requins/
├── index.html              # Fichier unique (HTML + CSS + JS)
├── README.md               # Ce fichier
└── LICENSE                 # Licence MIT
```

Le projet est volontairement **mono-fichier** pour faciliter le déploiement et l'utilisation hors ligne.

---

## 🛠️ Stack technique

| Composant | Bibliothèque | Version |
|---|---|---|
| Cartographie | [Leaflet](https://leafletjs.com/) | 1.9.4 |
| Graphiques | [Chart.js](https://www.chartjs.org/) | 4.4.1 |
| Export PDF | [jsPDF](https://github.com/parallax/jsPDF) | 2.5.1 |
| Tableaux PDF | [jsPDF-AutoTable](https://github.com/simonbengtsson/jsPDF-AutoTable) | 3.8.2 |
| Icônes | [Font Awesome](https://fontawesome.com/) | 6.7.2 |

---

## ⚠️ Limites et avertissements

### Limites techniques

- **Pas d'API temps réel** : les données officielles de vigies, drones et BSAN ne sont pas accessibles sans convention avec le CSR ou Ressac.
- **Dorsal** : plateforme collaborative sans API publique. Les signalements ne peuvent pas être intégrés automatiquement.
- **Données historiques** : basées sur des sources publiques, peuvent contenir des lacunes ou des imprécisions.

### Avertissements

> **Cet outil ne fournit pas d'alertes en temps réel à valeur réglementaire.**
> Pour toute décision de baignade ou d'activité nautique, consultez les **autorités locales** et l'application **Dorsal**.

> **Cet outil n'est pas affilié au CSR, à l'État français ou à Ressac.**
> Il s'agit d'un projet tiers indépendant à vocation informative et éducative.

> **Les données présentées peuvent être incomplètes ou obsolètes.**
> Vérifiez toujours les informations auprès des sources officielles.

---

## 🗺️ Feuille de route

### Court terme

- [ ] Enrichir la base d'attaques (compléter les 62 accidents recensés par le CSR)
- [ ] Ajouter un simulateur de risque (spot + heure + activité + météo)
- [ ] Intégrer les données de pluviométrie (turbidité)
- [ ] Ajouter un mode "comparateur temporel"

### Moyen terme

- [ ] Demander les données brutes du CSR via la CADA
- [ ] Intégrer les cartographies IRRAE (ADN environnemental)
- [ ] Ajouter les données du programme CHARC (marquage acoustique)
- [ ] Intégrer les signalements Dorsal (veille automatisée)

### Long terme

- [ ] API publique pour les développeurs
- [ ] Application mobile (PWA)
- [ ] Version multilingue (créole, anglais)
- [ ] Tableau de bord temps réel avec convention CSR

---

## 🤝 Contribuer

Les contributions sont les bienvenues ! Voici comment procéder :

1. **Fork** le dépôt
2. **Créez une branche** (`git checkout -b feature/ma-fonctionnalite`)
3. **Committez** vos changements (`git commit -m 'Ajout de ma fonctionnalité'`)
4. **Pushez** la branche (`git push origin feature/ma-fonctionnalite`)
5. **Ouvrez une Pull Request**

### Types de contributions recherchées

- 🐛 Correction de bugs
- 📊 Ajout de données historiques
- 🗺️ Amélioration de la carte
- 📈 Nouveaux graphiques ou analyses
- 📝 Documentation
- 🌍 Traductions

### Signaler un problème

Ouvrez une **issue** avec :

- Description du problème
- Étapes de reproduction
- Navigateur et version
- Captures d'écran si pertinent

---

## 📄 Licence

Ce projet est distribué sous licence **MIT**. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

```
MIT License

Copyright (c) 2026 Vigie Requins — La Réunion

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Remerciements

### Sources de données

- **Centre Sécurité Requin (CSR)** — pour les rapports publics sur les attaques et la pêche préventive
- **IRD / MARBEC** — pour les programmes CHARC et les études acoustiques
- **Shark Citizen / OFB** — pour le projet ReMaCAP
- **IUCN** — pour les données 2024 sur les captures
- **Dorsal** — pour la plateforme collaborative de signalement

### Bibliothèques open source

- **Leaflet** — cartographie interactive
- **Chart.js** — visualisation de données
- **jsPDF** — génération de PDF
- **Font Awesome** — icônes

### Communauté

- Les surfeurs, plongeurs et pêcheurs de La Réunion
- Les associations environnementales qui documentent les controverses
- Les chercheurs qui publient en open access

---

<div align="center">

**🦈 Vigie Requins — La Réunion**

*Outil tiers indépendant — non gouvernemental*

[⬆ Retour en haut](#-vigie-requins--la-réunion)

</div>

---

<div align="center">

### 🇪🇺 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>Gunout</strong> — Tous droits réservés.</sub>

</div>
