# Clartis Analytique — Site web

Site de présentation de **Clartis Analytique**, firme de tableaux de bord Power BI basée au Québec.

## Structure des fichiers

```
clartis-site/
├── index.html        ← Page d'accueil
├── services.html     ← Services & tarification
├── a-propos.html     ← À propos
├── contact.html      ← Formulaire de contact & FAQ
├── style.css         ← Styles partagés
└── README.md         ← Ce fichier
```

## Avant de déployer — Personnaliser

Avant de publier, remplacer les éléments entre `[ ]` :

1. **contact.html** → remplacer `[ votre@courriel.ca ]` et `[ votre numéro ]`
2. **Toutes les pages** → remplacer `clartis.ca` dans le footer par votre vrai domaine
3. **contact.html** → configurer le formulaire (voir ci-dessous)

### Configurer le formulaire de contact

Le formulaire n'envoie pas de courriel par défaut. Deux options simples :

**Option A — Formspree (gratuit)**
1. Créer un compte sur [formspree.io](https://formspree.io)
2. Créer un formulaire et copier votre endpoint
3. Dans `contact.html`, remplacer `action="#"` par `action="https://formspree.io/f/VOTRE_ID"`

**Option B — Netlify Forms**
Si vous hébergez sur Netlify, ajouter simplement `netlify` dans la balise `<form>`.

---

## Déployer sur GitHub Pages

### Étape 1 — Créer le dépôt GitHub

1. Aller sur [github.com](https://github.com) et se connecter
2. Cliquer sur le **+** en haut à droite → **New repository**
3. Nommer le dépôt : `clartis-site` (ou `votre-nom.github.io` pour un site principal)
4. Choisir **Public** (requis pour GitHub Pages gratuit)
5. Cliquer **Create repository**

### Étape 2 — Uploader les fichiers

**Méthode simple (sans terminal) :**

1. Dans votre nouveau dépôt, cliquer **Add file** → **Upload files**
2. Glisser-déposer tous les fichiers du dossier `clartis-site/`
3. Cliquer **Commit changes**

**Méthode terminal (si vous avez Git installé) :**
```bash
cd clartis-site
git init
git add .
git commit -m "Premier déploiement Clartis"
git branch -M main
git remote add origin https://github.com/VOTRE_NOM/clartis-site.git
git push -u origin main
```

### Étape 3 — Activer GitHub Pages

1. Dans votre dépôt GitHub, aller dans **Settings** (onglet en haut)
2. Dans le menu de gauche, cliquer **Pages**
3. Sous **Source**, sélectionner **Deploy from a branch**
4. Choisir la branche **main** et le dossier **/ (root)**
5. Cliquer **Save**

### Étape 4 — Accéder à votre site

Après 1–2 minutes, votre site sera disponible à :
```
https://VOTRE_NOM.github.io/clartis-site/
```

GitHub vous affichera l'URL exacte dans la section Pages de Settings.

---

## Mettre à jour le site

Pour modifier votre site après déploiement :

**Via GitHub (simple) :**
1. Ouvrir le fichier à modifier dans GitHub
2. Cliquer l'icône crayon (Edit)
3. Faire vos modifications
4. Cliquer **Commit changes**
5. Le site se met à jour automatiquement en ~1 minute

**Via terminal :**
```bash
# Après modification des fichiers locaux
git add .
git commit -m "Mise à jour"
git push
```

---

## Domaine personnalisé (optionnel)

Pour utiliser `clartis.ca` au lieu de `github.io` :

1. Acheter votre domaine (ex: sur [namecheap.com](https://namecheap.com))
2. Dans GitHub Pages Settings → **Custom domain** → entrer votre domaine
3. Chez votre registraire de domaine, configurer les DNS :
   ```
   Type: CNAME
   Nom: www
   Valeur: VOTRE_NOM.github.io
   ```
4. Cocher **Enforce HTTPS** dans GitHub Pages Settings

---

## Couleurs & identité

| Token      | Hex       | Usage                    |
|------------|-----------|--------------------------|
| Marine     | `#102A43` | Couleur principale       |
| Corail     | `#FF6B4A` | Accent, CTA              |
| Lime       | `#8FBF2E` | Éclat, indicateurs positifs |
| Marine nuit| `#0E2243` | Fonds sombres            |
| Brume      | `#F4F7FA` | Sections claires         |

**Polices :**
- Display : Bricolage Grotesque (800)
- Corps : Inter (400, 500, 600)
- Mono : IBM Plex Mono (400, 500)

---

*Clartis Analytique · Québec, Canada · L'essentiel, d'un seul coup d'œil.*
