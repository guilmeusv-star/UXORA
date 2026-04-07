# UXORA — La Maison des Génies

## 📁 ÉTAPE 1 — Organisation des fichiers

Crée un dossier sur ton bureau appelé `uxora-site`.
Mets TOUS ces fichiers dedans, dans le même dossier :

```
uxora-site/
│
├── uxora.html                         ✅ le site
├── README.md                          ✅ ce fichier
│
├── UXORA_NEW_DESIGNE.png              🖼️ image 1
├── PHOTO-2026-02-25-13-31-46_2.jpg   🖼️ image 2 — Masse Smoothie
├── PHOTO-2026-02-25-13-31-46_3.jpg   🖼️ image 3 — Puma Lafrancé
├── PHOTO-2026-02-25-13-31-46_4.jpg   🖼️ image 4 — Hamburger
├── PHOTO-2026-02-25-13-31-46_5.jpg   🖼️ image 5 — Jumex
├── PHOTO-2026-02-25-13-31-46_6.jpg   🖼️ image 6 — Jean Paul Gaultier
└── PHOTO-2026-02-25-13-31-46_7.jpg   🖼️ image 7 — Olly Magazine
```

⚠️ IMPORTANT : Les noms des fichiers images doivent être EXACTEMENT comme ci-dessus.
Ne renomme pas les fichiers. Une seule lettre différente = image invisible.

---

## 🌐 ÉTAPE 2 — Ouvrir le site

1. Ouvre le dossier `uxora-site`
2. Double-clique sur `uxora.html`
3. Le site s'ouvre dans ton navigateur (Chrome, Firefox, Edge...)
4. Toutes les images apparaissent automatiquement

---

## ➕ ÉTAPE 3 — Ajouter une nouvelle image dans la galerie

1. Copie ta nouvelle image dans le dossier `uxora-site`
2. Ouvre `uxora.html` avec **Notepad** (clic droit → Ouvrir avec → Notepad)
3. Cherche le texte `<!-- CRÉATIONS -->` dans le fichier
4. Copie ce bloc et colle-le juste avant `</div>` à la fin de la grille :

```html
<div class="creation-card" data-category="fashion" data-index="8">
  <img src="NOM-DE-TON-IMAGE.jpg" alt="Titre" loading="lazy">
  <div class="card-overlay">
    <h3>TITRE DE LA CRÉATION</h3>
    <p>Description courte</p>
    <span class="card-tag">Fashion</span>
  </div>
</div>
```

5. Remplace :
   - `NOM-DE-TON-IMAGE.jpg` → le vrai nom de ton fichier image
   - `TITRE DE LA CRÉATION` → le nom que tu veux afficher
   - `Description courte` → une ligne de description
   - `fashion` (dans data-category) → la catégorie : `fashion` / `food` / `branding` / `parfum`
   - `data-index="8"` → mets le numéro suivant (8, 9, 10...)

---

## 🎨 ÉTAPE 4 — Personnaliser les couleurs

Ouvre `uxora.html` avec Notepad, cherche ce bloc tout en haut :

```css
:root {
  --green: #1d9e75;        /* couleur principale verte */
  --green-light: #5dcaa5;  /* vert clair accent */
  --dark: #0b1f2a;         /* fond sombre */
}
```

Change les codes couleur selon tes préférences.

---

## 📞 ÉTAPE 5 — Changer le numéro WhatsApp

Ouvre `uxora.html` avec Notepad.
Cherche (Ctrl+H) : `50931656011`
Remplace par ton numéro (sans + ni espaces, avec indicatif pays).
Ex: Haiti +509 → `50912345678`

---

## 📱 Réseaux sociaux UXORA

| Plateforme | Compte |
|---|---|
| WhatsApp | +509 3165 6011 |
| Instagram | @UXORA04 |
| Facebook | Trevor Phillips |
| TikTok | @UXORA7 / @UXORALMGGRAPHISTE |

---

## ❓ Problèmes fréquents

| Problème | Solution |
|---|---|
| Les images n'apparaissent pas | Vérifie que les images sont dans le même dossier que `uxora.html` |
| Le nom de l'image est incorrect | Vérifie qu'il n'y a pas d'espace ou de majuscule en trop |
| Le site ne s'ouvre pas | Clic droit sur `uxora.html` → Ouvrir avec → Chrome ou Firefox |
| Une image manque | Vérifie le nom exact du fichier dans le dossier |

---

*UXORA — La Maison des Génies · Design Graphique · Port-au-Prince, Haïti*
