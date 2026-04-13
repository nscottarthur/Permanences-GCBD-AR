# Bridges AR — CAP IMT Mines Alès

Viewer 3D + AR pour les modèles de ponts à treillis. À déployer sur GitHub Pages.

---

## Étape 1 — Télécharger les modèles Sketchfab

Télécharge les deux modèles en format **.glb** depuis Sketchfab (bouton "Download" → choisir GLB ou GLTF) :

- **v1** → https://sketchfab.com/3d-models/bridge-truss-structure-3cecc079502a4092956188c79655f0d5
- **v2** → https://sketchfab.com/3d-models/bridge-truss-structure-d1763b1dacb24a0795f640f1801dac40

Renomme-les en :
- `bridge1.glb`
- `bridge2.glb`

Place ces deux fichiers dans le même dossier que `index.html`.

---

## Étape 2 — Mettre à jour les chemins dans index.html

Dans `index.html`, repère ce bloc JS et remplace les deux `src` :

```js
const MODELS = [
  {
    src: 'bridge1.glb',   // ← changer ici
    ...
  },
  {
    src: 'bridge2.glb',   // ← changer ici
    ...
  }
];
```

---

## Étape 3 — Déployer sur GitHub Pages

1. Crée un nouveau dépôt GitHub (ex: `bridges-ar`)
2. Ajoute tous les fichiers :
   - `index.html`
   - `qr.html`
   - `bridge1.glb`
   - `bridge2.glb`
3. Dans Settings → Pages → Source : **main branch / root**
4. GitHub génère une URL du type : `https://TON-USERNAME.github.io/bridges-ar/`

---

## Étape 4 — Mettre à jour le QR code

Dans `qr.html`, ligne 1 du script, remplace :

```js
const TARGET_URL = 'https://VOTRE-USERNAME.github.io/bridges-ar/';
```

par ton URL réelle, puis re-push.

---

## Étape 5 — Imprimer le QR

Ouvre `qr.html` dans le navigateur → Ctrl+P / Cmd+P → Imprimer.
Coupe et pose sur les tables avant la permanence.

---

## Notes

- L'AR fonctionne nativement sur iOS (Quick Look) et Android (Scene Viewer / WebXR)
- Les modèles `.glb` doivent être sur le même domaine (GitHub Pages) — pas de CDN externe
- Si les fichiers .glb sont trop lourds (>20 Mo), compresse avec https://gltf.report/
