# 📘 Guide d'utilisation - Système de gestion du site

## 🎯 Vue d'ensemble

Ce système vous permet de **modifier facilement le contenu du site** en éditant des fichiers JSON, puis de **générer automatiquement** le fichier `index.html`.

## 📁 Structure des fichiers

```
13_node_Ed/
├── data/                      # 📊 VOS DONNÉES (à modifier)
│   ├── site.json             # Contenu général du site
│   └── couteaux.json         # Liste des couteaux
├── templates/                 # 🎨 Templates HTML (à créer)
│   └── template.html         # Template principal
├── build.js                   # ⚙️ Script de génération
├── package.json              # Configuration Node.js
├── index.html                # ✅ Site généré (ne pas modifier manuellement)
├── couteaux.html             # 📝 Backup/référence
└── medias/                   # 🖼️ Images et vidéos
```

## 🚀 Utilisation rapide

### 1️⃣ Modifier les données

Éditez les fichiers JSON dans le dossier `data/` :

**`data/site.json`** - Contenu général :
- Titre, description, contact
- Sections (Process, Matériaux, À propos, etc.)
- Navigation
- Textes et descriptions

**`data/couteaux.json`** - Galerie de couteaux :
- Nom, description, prix
- Image, disponibilité
- Facile à ajouter/modifier/supprimer

### 2️⃣ Générer le site

```bash
# Méthode 1 : Avec npm
npm run build

# Méthode 2 : Directement avec Node.js
node build.js
```

### 3️⃣ Déployer sur GitHub

```bash
# Méthode automatique
npm run deploy

# Méthode manuelle
git add index.html
git commit -m "Mise à jour du site"
git push
```

## 📝 Exemples de modifications

### Ajouter un couteau

Éditez `data/couteaux.json` :

```json
{
  "id": 11,
  "name": "Nouveau Couteau",
  "description": "Description du couteau...",
  "price": "300€",
  "image": "medias/Capture_11.JPG",
  "available": true
}
```

### Modifier une section

Éditez `data/site.json` :

```json
"process": {
  "title": "Nouveau titre",
  "description": "Nouvelle description...",
  "items": [...]
}
```

### Changer les informations de contact

Éditez `data/site.json` :

```json
"meta": {
  "email": "nouveau@email.fr",
  "instagram": "https://www.instagram.com/nouveau_compte/"
}
```

## ⚠️ Règles importantes

1. ✅ **Modifiez UNIQUEMENT les fichiers JSON** dans `data/`
2. ❌ **NE modifiez PAS `index.html` manuellement** (il sera écrasé)
3. ✅ **Utilisez `couteaux.html` comme référence** si besoin
4. ✅ **Testez localement** avant de déployer
5. ✅ **Faites des sauvegardes** de vos fichiers JSON

## 🔧 Commandes disponibles

```bash
npm run build    # Génère index.html
npm run dev      # Génère et affiche un message
npm run deploy   # Génère, commit et push sur GitHub
```

## 📊 Format des données

### Couteau (couteaux.json)

```json
{
  "id": 1,                              // Numéro unique
  "name": "Nom du couteau",             // Titre
  "description": "Description...",       // Texte descriptif
  "price": "350€",                      // Prix (texte libre)
  "image": "medias/photo.JPG",          // Chemin de l'image
  "available": true                     // true = disponible, false = sur commande
}
```

### Section Process/Materials (site.json)

```json
{
  "title": "Titre de la section",
  "description": "Description...",
  "items": [
    {
      "title": "Titre de l'item",
      "text": "Texte...",
      "animation": "fade-in-scroll"    // ou "slide-in-left", "slide-in-right"
    }
  ]
}
```

## 🎨 Animations disponibles

- `fade-in-scroll` - Apparition en fondu
- `slide-in-left` - Glissement depuis la gauche
- `slide-in-right` - Glissement depuis la droite

## 🆘 Aide

Si vous avez des questions ou des problèmes :
1. Vérifiez que les fichiers JSON sont valides (pas d'erreur de syntaxe)
2. Relancez `node build.js` pour voir les erreurs
3. Consultez `couteaux.html` pour voir la structure actuelle

## 📌 Prochaines étapes

Le script `build.js` est actuellement en développement. Il va :
- ✅ Charger les données JSON
- 🔄 Générer le HTML complet (en cours)
- 🔄 Créer le template (à faire)
- 🔄 Gérer les animations (à faire)

