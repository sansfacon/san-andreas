# Gouvernement de San Andreas — Portail officiel

Site web pour serveur FiveM RP : page publique, plan de vol interactif,
espace sécurisé (documents, signature électronique, entreprises, administration).

## Démarrer en local

```bash
npm install
npm run dev
```

Puis ouvrir http://localhost:3000

## Identifiants par défaut

- Identifiant : `admin`
- Mot de passe : `admin123`

Ce compte est créé automatiquement au premier chargement du site (stocké dans le
navigateur). Pense à changer le mot de passe ou à créer d'autres comptes depuis
la page Administration.

## Stockage des données

Ce projet ne nécessite AUCUNE base de données : tout (utilisateurs, documents,
entreprises, notifications) est stocké dans le navigateur via `localStorage`.
C'est volontairement simple pour un déploiement instantané sans configuration.

Limite à connaître : les données sont propres à chaque navigateur / appareil,
elles ne sont pas partagées entre les membres du gouvernement. Si tu as besoin
d'une base partagée plus tard (PostgreSQL, etc.), il faudra remplacer le contenu
de `lib/store.ts` par des appels à une API — demande-le et on fera l'étape suivante.

## Déploiement sur Vercel

Voir les instructions données par Claude dans la conversation, ou simplement :

1. Créer un dépôt GitHub avec ce code
2. Aller sur vercel.com → New Project → importer le dépôt
3. Laisser les réglages par défaut (Next.js est détecté automatiquement)
4. Cliquer sur Deploy
