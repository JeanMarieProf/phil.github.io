# 🧩 Composants Réutilisables - Classification

> **Note :** Ce document identifie les patterns et composants du template `couteaux.html` pour la factorisation future.

---

## 📋 **Vue d'ensemble**

Le template contient **10 sections principales** + **composants transversaux** (header, footer, modale).

---

## 🎨 **1. COMPOSANTS DE NAVIGATION**

### **1.1 Header / Navigation**
- **Localisation :** Lignes ~1150-1163
- **Type :** Navigation fixe responsive
- **Caractéristiques :**
  - Logo cliquable
  - Menu horizontal (desktop)
  - Menu hamburger (mobile)
  - Backdrop blur effect
  - Sticky positioning
- **Réutilisable pour :** Tous types de sites

### **1.2 Footer**
- **Localisation :** Lignes ~1640-1680
- **Type :** Footer avec liens et infos
- **Caractéristiques :**
  - Liens de navigation
  - Informations de contact
  - Réseaux sociaux
  - Copyright
- **Réutilisable pour :** Tous types de sites

---

## 🖼️ **2. COMPOSANTS HERO**

### **2.1 Hero avec Parallaxe**
- **Localisation :** Lignes 1165-1172
- **Type :** Section plein écran avec effet parallaxe
- **Caractéristiques :**
  - Background vidéo/image
  - Overlay sombre
  - Titre + sous-titre centré
  - Effet parallaxe au scroll (JS lignes ~1787-1857)
  - Hauteur 100vh
- **Réutilisable pour :** Sites portfolio, landing pages, sites produits

---

## 🛍️ **3. COMPOSANTS PRODUITS/GALERIE**

### **3.1 Slider de Produits (Couteaux)**
- **Localisation :** Lignes 1175-1380
- **Type :** Carrousel de produits avec navigation
- **Caractéristiques :**
  - Slides avec image + texte
  - Boutons prev/next
  - Navigation par points
  - Bouton "Acheter"
  - Responsive (vertical sur mobile)
  - JavaScript slider (lignes ~1690-1750)
- **Réutilisable pour :** E-commerce, portfolios, galeries produits

### **3.2 Galerie d'Images Simple**
- **Localisation :** Section #objets (lignes 1478-1488)
- **Type :** Grille d'images avec légendes
- **Caractéristiques :**
  - Images avec `<figure>` et `<figcaption>`
  - Layout en grille
  - Animation fade-in au scroll
- **Réutilisable pour :** Portfolios, galeries photo

### **3.3 Diaporama GIF**
- **Localisation :** Section #diaporama (lignes 1468-1476)
- **Type :** Image/GIF pleine largeur
- **Caractéristiques :**
  - Image centrée
  - Wrapper avec animation
- **Réutilisable pour :** Démonstrations, animations

---

## 📊 **4. COMPOSANTS PROCESSUS/ÉTAPES**

### **4.1 Grille de Processus**
- **Localisation :** Section #process (lignes 1382-1409)
- **Type :** Grille d'étapes avec média + texte
- **Caractéristiques :**
  - 3 colonnes (responsive)
  - Chaque item : image/vidéo + titre + description
  - Animations différenciées (slide-in-left, fade, slide-in-right)
  - Support vidéo autoplay
- **Réutilisable pour :** Tutoriels, processus de fabrication, étapes de service

---

## 🏷️ **5. COMPOSANTS CARTES/LISTES**

### **5.1 Cartes de Matériaux**
- **Localisation :** Section #materials (lignes 1411-1450)
- **Type :** Cartes avec listes à puces
- **Caractéristiques :**
  - 3 colonnes (responsive)
  - Titre de carte
  - Liste d'items (nom + description)
  - Footer explicatif
  - Animations slide-in
- **Réutilisable pour :** Caractéristiques produits, services, technologies

---

## 👤 **6. COMPOSANTS À PROPOS**

### **6.1 Section About (Image + Texte)**
- **Localisation :** Section #about (lignes 1490-1507)
- **Type :** Layout 2 colonnes (image + texte)
- **Caractéristiques :**
  - Image à gauche (logo/photo)
  - Texte à droite (titre + paragraphes)
  - Responsive (vertical sur mobile)
  - Animations slide-in opposées
- **Réutilisable pour :** Pages à propos, biographies, présentations

---

## 🔗 **7. COMPOSANTS INTÉGRATIONS EXTERNES**

### **7.1 Widget Instagram**
- **Localisation :** Section #instagram (lignes 1509-1553)
- **Type :** Intégration iframe Instagram
- **Caractéristiques :**
  - Embed officiel Instagram
  - Dimensions configurables
  - Lien vers le profil
  - Centré et responsive
- **Réutilisable pour :** Intégrations réseaux sociaux

### **7.2 Google Maps**
- **Localisation :** Section #contact (lignes 1555-1639)
- **Type :** Carte Google Maps intégrée
- **Caractéristiques :**
  - iframe Google Maps
  - Layout 2 colonnes (infos + carte)
  - Responsive
- **Réutilisable pour :** Pages contact, localisation

---

## 💬 **8. COMPOSANTS INTERACTIFS**

### **8.1 Modale de Contact**
- **Localisation :** Lignes 1681-1730
- **Type :** Modale overlay avec formulaire
- **Caractéristiques :**
  - Overlay sombre
  - Formulaire de contact
  - Bouton fermeture
  - JavaScript pour ouvrir/fermer (lignes ~1751-1786)
  - Fermeture au clic extérieur
- **Réutilisable pour :** Formulaires, popups, confirmations

---

## ⚙️ **9. COMPOSANTS JAVASCRIPT**

### **9.1 Menu Mobile Toggle**
- **Localisation :** JS lignes ~1690
- **Fonction :** Ouvrir/fermer le menu hamburger
- **Réutilisable pour :** Tous sites responsive

### **9.2 Slider/Carrousel**
- **Localisation :** JS lignes ~1690-1750
- **Fonction :** Navigation entre slides
- **Réutilisable pour :** Galeries, produits, témoignages

### **9.3 Effets Parallaxe**
- **Localisation :** JS lignes ~1787-1857
- **Fonction :** Animations au scroll
- **Caractéristiques :**
  - Parallaxe hero (background + content)
  - Fade-in au scroll
  - Slide-in left/right
  - Optimisé avec `requestAnimationFrame`
- **Réutilisable pour :** Sites modernes avec animations

---

## 📐 **10. PATTERNS CSS RÉUTILISABLES**

### **10.1 Variables CSS (Design Tokens)**
- **Localisation :** Lignes 11-21
- **Contenu :** Couleurs, fonts
- **Réutilisable pour :** Système de thèmes

### **10.2 Animations CSS**
- **Localisation :** Lignes 185-279
- **Types :**
  - `.fade-in-scroll`
  - `.slide-in-left`
  - `.slide-in-right`
- **Réutilisable pour :** Tous sites avec animations

### **10.3 Responsive Breakpoints**
- **Localisation :** Media queries lignes ~900-1150
- **Breakpoints :**
  - 992px (desktop)
  - 768px (tablet)
  - 480px (mobile)
- **Réutilisable pour :** Tous sites responsive

---

## 🎯 **CLASSIFICATION PAR TYPE DE SITE**

### **Site E-commerce / Produits**
- ✅ Header navigation
- ✅ Hero avec parallaxe
- ✅ Slider de produits
- ✅ Grille de processus (fabrication)
- ✅ Cartes de matériaux (caractéristiques)
- ✅ Section about
- ✅ Modale de contact
- ✅ Footer

### **Portfolio / Artiste**
- ✅ Header navigation
- ✅ Hero avec parallaxe
- ✅ Galerie d'images
- ✅ Section about
- ✅ Widget Instagram
- ✅ Modale de contact
- ✅ Footer

### **Landing Page / Service**
- ✅ Header navigation
- ✅ Hero avec parallaxe
- ✅ Grille de processus (étapes)
- ✅ Cartes (services/features)
- ✅ Section about (équipe)
- ✅ Google Maps (localisation)
- ✅ Modale de contact
- ✅ Footer

---

## 📝 **PROCHAINES ÉTAPES (Factorisation)**

1. **Extraire les composants** dans `components/`
2. **Créer des layouts** dans `templates/layouts/`
3. **Créer un système de thèmes** dans `themes/`
4. **Paramétrer via JSON** les composants utilisés
5. **Générer dynamiquement** selon la config

**Exemple de config future :**
```json
{
  "layout": "single-page",
  "components": [
    { "type": "hero-parallax", "data": "..." },
    { "type": "product-slider", "data": "..." },
    { "type": "process-grid", "data": "..." }
  ]
}
```

