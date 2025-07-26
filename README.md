# Food & Drinks Ratings (FDR)

Une **Progressive Web App (PWA)** pour noter et partager vos avis sur les **restaurants** et **bars** entre amis, avec une stack moderne et 100 % gratuite.

> **Démo en ligne bientôt disponible**  
> *Gratuit à vie* grâce aux offres gratuites de **Netlify** et **Supabase**.

---

## ✨ Fonctionnalités

| Catégorie             | Essentielles                                 | Prévu (à venir)                      |
| --------------------- | -------------------------------------------- | ------------------------------------ |
| **Comptes & Social**  | Connexion Email / OAuth, liste d’amis         | Invitations de groupe, rôles admin   |
| **Lieux**             | Deux types (Restaurant / Bar), adresse + map | Import via Google Places API         |
| **Notes & Avis**      | 1–5 ⭐, texte, photos, file d’attente offline | Tags (veggie, cosy…), recherche      |
| **Statistiques**      | Moyenne, classements                         | Badges, tendances hebdo              |
| **PWA**               | Installable, cache offline, background sync  | Notifications push                   |

---

## 🏗️ Stack Technique

| Couche                   | Outil / Service                            | Avantage                           | Offre gratuite                                  |
| ------------------------ | ------------------------------------------ | ---------------------------------- | ----------------------------------------------- |
| **UI / Framework**       | **React 18** (Next.js 14 – *app router*)   | SEO, ISR, routage par fichiers     | Open‑source                                     |
| **Style**                | Tailwind CSS + shadcn/ui                   | Thématisation rapide, accessibilité| Open‑source                                     |
| **État & Données**       | TanStack Query + Zod                       | Cache & validation                 | Open‑source                                     |
| **Backend‑as‑a‑Service** | **Supabase** (Postgres, Auth, Storage)     | Temps réel, quotas généreux        | 500 MB DB, 1 GB fichiers, 50k MAU               |
| **Hébergement**          | **Netlify**                                | CDN global rapide, CI/CD            | 100 GB bande passante, 300 min build, 125k calls |
| **Images**               | Cloudinary                                 | Optimisation & CDN images           | 25 GB stockage                                  |
| **Cartes (option)**      | Leaflet + OpenStreetMap                    | Alternative gratuite à Google Maps  | Gratuit                                         |

---

## 🚀 Démarrage rapide

```bash
# 1. Cloner & installer
npx create-next-app fdr --typescript --use-npm --tailwind
cd fdr
npm install @supabase/supabase-js @tanstack/react-query zod workbox-window

# 2. Variables d'environnement
cp .env.local.example .env.local
# Ajouter SUPABASE_URL / SUPABASE_ANON_KEY

# 3. Lancer le serveur
npm run dev
```

### Exemple `.env.local`

```env
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=public-anon-key
```

---

## 🌐 Déploiement sur Netlify

1. Pousser le code sur GitHub.  
2. Se connecter à Netlify → **New site** → **Import from GitHub**.  
3. Configurer les *Variables d’environnement* comme dans `.env.local`.  
4. Commande de build : `next build && next export` (statique) **ou** activer le runtime Next.js.  
5. Dossier de publication : `out` (export statique) ou vide pour hybride.  
6. Activer les *en-têtes PWA* dans **Netlify → Site Settings → Headers & redirects**.

> Dès le premier déploiement, l’app sera installable (Chrome 87+, Safari 17+) et utilisable hors-ligne.

---

## 💰 Stratégie Free‑Tier

| Service        | Quotas (2025)                                     | Pourquoi suffisant ?                   |
| -------------- | ------------------------------------------------- | -------------------------------------- |
| **Netlify**    | 100 GB/mo, 300 min build, 125k functions           | Suffisant pour un usage entre amis     |
| **Supabase**   | 500 MB DB, 1 GB fichiers, 50k MAU                  | Gère ~10k avis/photos avant upgrade    |
| **Cloudinary** | 25 GB stockage, 25 GB CDN, 100 MB/img              | Idéal pour des photos compressées      |
| **Neon** (opt) | 3 GB DB, 1 GB RAM                                  | Backup si Supabase devient trop juste  |

---

## 🗺️ Feuille de route

### Phase 0 – Setup *(Jour 0–1)*  
- [x] Choix stack (React/Next.js, Tailwind)  
- [x] Git + CI (lint, type-check)  
- [ ] Config Prettier, Husky, commitlint  

### Phase 1 – MVP *(Semaine 1–2)*  
- [ ] Projet Supabase + tables (`users`, `venues`, `reviews`, `categories`)  
- [ ] Auth (email magic link)  
- [ ] CRUD Lieux (restaurant, bar)  
- [ ] Composant note ⭐ + update optimiste  
- [ ] Manifest PWA + Workbox  

### Phase 2 – Offline & Médias *(Semaine 3–4)*  
- [ ] IndexedDB queue + Background Sync  
- [ ] Upload photos → Supabase Storage / Cloudinary  
- [ ] Analytics basiques (Netlify Insights)  

### Phase 3 – Social & Finitions *(Semaine 5–6)*  
- [ ] Système d’amis (follow/unfollow)  
- [ ] Leaderboards + graphiques  
- [ ] Mode sombre, audit a11y, Lighthouse > 90  

### Phase 4 – Bonus *(Plus tard)*  
- [ ] Notifications push (Web‑Push)  
- [ ] Import Google Places  
- [ ] Versions natives (Tauri / Capacitor)  

---

## 🤝 Contribuer

1. Fork → branche de fonctionnalité → PR.  
2. Respecter Conventional Commits, `npm run lint` avant push.  
3. Les *good first issues* sont marquées **help wanted**.

---

## 📄 Licence

MIT © 2025 *Votre Nom*
