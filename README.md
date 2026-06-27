# 📦 VerseL – Gestion Commerciale

**Version :** 1.0.0.0  
**Statut :** Production Ready  
**Type :** Application Web Progressive (PWA) 100 % hors ligne

---

## 🚀 Présentation

VerseL est une **application de gestion commerciale professionnelle** conçue pour les commerçants, boutiques, PME et entrepreneurs.  
Elle centralise la gestion des **ventes**, du **stock**, des **archives** et des **statistiques** dans une interface moderne, intuitive et entièrement fonctionnelle **sans connexion Internet**.

---

## ✨ Fonctionnalités principales

| Module | Fonctionnalités clés |
| :--- | :--- |
| **🏠 Accueil** | KPIs en temps réel (CA mensuel, bénéfice, stock), graphique de courbe des ventes (Chart.js), classement Top 10 des produits. |
| **💰 Ventes** | Formulaire intelligent avec auto-complétion, validation du stock, calcul automatique du total, modification/suppression, résumé journalier. |
| **📦 Stock** | CRUD complet, alertes de stock faible et rupture, tableau des statuts (Disponible / Stock faible / Rupture), valeur totale. |
| **🗂️ Données** | Archivage automatique à minuit, regroupement intelligent par date et produit, filtres de recherche, exports PDF et Excel. |
| **⚙️ Paramètres** | Modification du profil entreprise (Nom, Pays, Ville, Devise), bouton d'assistance WhatsApp, zone de réinitialisation complète. |
| **🌓 Thème** | Mode Clair, Mode Sombre, Mode Automatique (synchronisé avec le système). |

---

## 🛠️ Technologies utilisées

- **Frontend** : HTML5, CSS3, JavaScript Vanilla (ES6+)
- **Persistance** : `localStorage` (aucune base de données externe)
- **Bibliothèques CDN** :
  - [Chart.js](https://www.chartjs.org/) – Graphiques interactifs
  - [jsPDF](https://github.com/parallax/jsPDF) – Export PDF
  - [SheetJS](https://sheetjs.com/) – Export Excel
- **PWA** : `manifest.json` + `service-worker.js` (fonctionnalité hors ligne)

---

## 📁 Structure du projet
versel/
├── index.html # Application complète (HTML + CSS + JS)
├── manifest.json # Configuration PWA (icônes, thème, nom)
├── service-worker.js # Gestion du cache et du mode hors ligne
└── assets/
└── logo.png # Logo de l'application (192x192 et 512x512 recommandé)

---

## 🚦 Installation et exécution locale

> **⚠️ Important :** Pour que le Service Worker fonctionne, l'application doit être servie via **HTTPS** ou **localhost**. Une simple ouverture du fichier `index.html` dans le navigateur ne suffira pas à activer le mode hors ligne.

### 1. Téléchargement
Clonez ce dépôt ou téléchargez les fichiers dans un dossier nommé `versel`.

### 2. Lancer un serveur local (recommandé)
Si vous avez **Node.js** installé :
```bash
npx http-server ./versel -p 8080
