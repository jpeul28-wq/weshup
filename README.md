# Weshup ↑

L'IA bienveillante pour les jeunes. Jobs, études, avenir.

## Déploiement sur Render

### Étape 1 — GitHub
1. Crée un compte sur github.com si pas déjà fait
2. Crée un nouveau dépôt (repository) appelé `weshup`
3. Upload les fichiers `index.html` et `render.yaml`

### Étape 2 — Clé API Anthropic
1. Va sur console.anthropic.com
2. Crée une clé API
3. Copie la clé (commence par `sk-ant-...`)
4. Dans `index.html`, remplace `REMPLACE_PAR_TA_CLE_API` par ta vraie clé

### Étape 3 — Render
1. Va sur render.com
2. Connecte ton compte GitHub
3. "New" → "Static Site"
4. Sélectionne le dépôt `weshup`
5. Render détecte automatiquement le `render.yaml`
6. Clique "Deploy"

### Étape 4 — Domaine weshup.app
1. Dans Render → Settings → Custom Domain
2. Ajoute `weshup.app`
3. Render te donne un CNAME (ex: weshup.onrender.com)
4. Dans OVH → Zone DNS → Ajoute un enregistrement CNAME
   - Nom : `@` ou `weshup.app`
   - Valeur : `weshup.onrender.com`
5. Attendre 15-30 min pour la propagation DNS

## Stack technique
- Frontend : HTML/CSS/JS pur (pas de framework)
- IA : Anthropic API (claude-haiku-4-5)
- Hébergement : Render (Static Site, gratuit)
- Domaine : weshup.app (OVH)
- SSL : Automatique via Render

## Coût mensuel estimé
- Render Static Site : 0€
- Anthropic API (Haiku) : ~5-8€ selon trafic
- Domaine OVH : ~1.5€/mois (18€/an)
- **Total : ~7-10€/mois**
