# DryCups — Landing page

Landing page bilingue (FR/EN) pour DryCups : cupping traditionnel chinois (bàguàn) à Paris.
Site statique — un seul `index.html` + `images/` — animé avec GSAP ScrollTrigger et Lenis.

Implémenté depuis le design Claude Design « DryCups Landing.dc.html ».

## Développement

Aucun build. Ouvrir `index.html` dans un navigateur, ou :

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Déploiement

Chaque push sur `main` redéploie automatiquement le site sur GitHub Pages via
GitHub Actions (`.github/workflows/deploy.yml`).

- URL : https://pcangemi.github.io/drycups-site/
- Suivi des déploiements : onglet **Actions** du repo

## Connecter le domaine dry-cups.com (optionnel)

1. Chez le registrar (OVH, Namecheap, Cloudflare…), ajouter :

   | Type  | Nom | Valeur |
   |-------|-----|--------|
   | A     | @   | 185.199.108.153 |
   | A     | @   | 185.199.109.153 |
   | A     | @   | 185.199.110.153 |
   | A     | @   | 185.199.111.153 |
   | CNAME | www | `pcangemi.github.io` |

2. Repo → **Settings → Pages → Custom domain** : saisir `dry-cups.com`, puis
   cocher **Enforce HTTPS** (disponible après propagation DNS, 5 min à 24 h).
