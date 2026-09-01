# Portfolio — Ayman Dahraoui

Portfolio personnel en **un seul fichier** : `index.html` (HTML + CSS + JavaScript, sans build ni dépendance npm).

## Structure

```
Portfolio/
├── index.html                     # tout le site (structure, styles, scripts)
├── assets/
│   ├── CV-Ayman-Dahraoui.pdf      # CV téléchargé par le bouton "Télécharger CV"
│   └── photo.jpg                  # (à ajouter) photo de profil — sinon "AD" s'affiche
└── README.md
```

## Personnalisation rapide

| Quoi | Où dans `index.html` |
|---|---|
| Couleurs (bleu `#00D4FF` / violet `#7C3AED`) | bloc `:root` en haut du `<style>` |
| Phrases du typing effect | tableau `roles` dans le `<script>` |
| Lien du CV | `assets/CV-Ayman-Dahraoui.pdf` (section Hero) |
| Photo | déposer `assets/photo.jpg` — le fallback initiales disparaît automatiquement |
| Densité des particules | `Math.min(90, ...)` dans la fonction `resize()` |

## Formulaire de contact

Par défaut il ouvre le client mail (`mailto:`) avec le message pré-rempli — aucun backend requis.

Pour recevoir les messages directement par email, créer un formulaire sur [formspree.io](https://formspree.io)
puis remplacer le bloc `form.addEventListener('submit', ...)` par un `fetch()` vers l'endpoint fourni.

## Mise en ligne

**GitHub Pages**
```bash
git init && git add . && git commit -m "portfolio"
git branch -M main
git remote add origin https://github.com/ayman-dahraoui/portfolio.git
git push -u origin main
# puis Settings → Pages → Branch: main / root
```

**Netlify / Vercel** : glisser-déposer le dossier, aucune configuration nécessaire.

## Aperçu local

Ouvrir `index.html` dans le navigateur, ou :
```bash
python -m http.server 8000
```
