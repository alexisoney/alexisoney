---
sidebar_position: 3
---

# Pelostudio

**Rôle :** Frontend Developer / Lead Process / Recrutement

**Tech & outils :** React, TypeScript, SCSS/Tailwind, Figma, Specify, Storyblok, ESLint, Prettier, Husky, GitHub Actions

---

### 🔍 Contexte

Quand j'ai rejoint Pelostudio, l'équipe développement était composée de deux personnes. J'étais le deuxième dev front, avec une forte appétence pour la structuration technique et la collaboration design-dev.

Durant mes trois années, nous avons livré 35 sites web headless pour des clients SaaS. Cette cadence exigeait des workflows ultra-efficients.

### Problèmes identifiés au départ :

- Temps perdu sur chaque lancement de projet (jusqu'à 1 jour) pour récupérer couleurs, fonts, icônes, créer les mixins, etc.
- Risque d’oubli ou d’erreurs lors de mises à jour de styles pendant un projet.
- Nomenclature non alignée entre dev et design, ce qui ralentissait l’implémentation.
- Code non harmonisé entre les membres de l’équipe (pas de linter, pas de check PR, erreurs en production).

### Objectifs visés :

- Gagner du temps sur les setup projets.
- Réduire les erreurs de transfert design → code.
- Poser une base commune dev/design (naming, composants, structure).
- Améliorer la qualité du code et les process de déploiement.

---

## 👥 Structuration de l'équipe

### Recrutement

- J'ai participé à la shortlist de profils à partir de CV et GitHub.
- Conception de tests techniques basés sur notre stack et nos besoins (site headless, créatif, pixel perfect).
- Participation à l'onboarding des devs, avec accompagnement des juniors via des revues de code, du mentorat, et la mise en place d'un cadre d'autonomie progressif.

### Équipe

- À terme, nous étions 5 développeurs frontend orientés "headless website" (notamment avec Storyblok).

---

## 🎨 Collaboration Design ⇄ Dev

### Frictions rencontrées :

- Les composants étaient souvent similaires d’un projet à l’autre (ex : Hero avec Kicker, Title, Description, Button), mais les variations tardives (ex : ajout d’un 2e bouton) étaient chronophages.
- L'import manuel des fonts, icônes et styles était long, sensible aux erreurs et source de frictions.
- L’absence de nomenclature commune complexifiait la communication entre designers et développeurs.

### Solution : Specify

- Specify était un outil qui synchronisait automatiquement les local styles Figma (couleurs, fonts, icônes) avec nos fichiers SCSS ou Tailwind.
- Un simple `npm run specify` permettait de mettre à jour tout le design token sans effort manuel.

→ Lire mon interview sur le sujet : [How Pelostudio uses Specify](https://specifyapp.com/customer-stories/how-pelostudio-use-specify)

### Mise en place

- Collaboration étroite avec les designers pour nommer les styles et icônes.
- Rassemblement et classification des composants récurrents (design tokens, patterns).
- Formation de l’équipe design à Specify pour qu’ils puissent configurer les projets eux-mêmes.

### Résultats

- Setup projet passé de 1 journée à 1h.
- Moins d’erreurs, plus de fluidité, anticipation des besoins clients.
- Adoption quasi totale dans l’équipe : même les designers prenaient en main Specify.

---

## 🔧 Qualité du code & process dev

### Avant

- Aucun outil de formatage ou de lint.
- Risque de bugs ou de déploiements cassés tard dans le process.

### Mise en place

- Prettier pour le formating automatique
- ESLint pour le linting + règles personnalisées :
  - tri des imports
  - interdiction des `console.log`
  - gestion d’erreurs Typescript
- Husky pour les hooks pre-commit : vérification avant push
- GitHub Actions : 2e sécurité avant les pull-requests

### Adoption

- Rollout progressif sur les projets pilotés par les devs les plus expérimentés.
- Documentation + démo interne + grandes discussions d'équipe pour les conventions de nommage.
- Avec le temps, tous les projets ont convergé vers cette structure commune.

---

## 📊 Résultats

- Setup projets divisé par x7 en temps (de 1 jour à 1h).
- Build à 99% success sur tous les projets Netlify.
- Adoption forte de Specify jusqu’à sa fermeture.
- Designers et devs opérationnels sur des bases communes (même nomenclature, même pipeline).
- Devs autonomes avec une meilleure expérience DX (Husky, lint, preview safe).

---

## 🤓 Apprentissages

- Il faut parfois sacrifier un peu de liberté créative pour gagner en efficacité collective.
- Les outils tiers comme Specify sont puissants mais dépendants de leur roadmap : je ferais un jour mon propre plugin Figma si c’était à refaire.
- Tout le monde n’a pas la même affinité avec la rigueur nomenclature/design system : c’est une culture à construire avec de la pédagogie et de la diplomatie.
- Formaliser, documenter, présenter, montrer par l’exemple : c’est le meilleur levier pour faire adopter des process dans une équipe en croissance.
