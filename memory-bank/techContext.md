# Tech Context — environnement et contraintes techniques

## Environnement
- OS : Windows 11 (préparation) / machine de démo : à confirmer
- Éditeur : VS Code
- Repo : Markdown + (optionnel) projet Vite/Vue pour la démo
- Outils CLI présents : git, curl, python, dotnet, npm

## Démo — hypothèses techniques
- Le serveur MCP Gmail est **déjà configuré** avant la présentation (OAuth OK).
- Le scaffold **Vite + Vue** est prêt avant l’atelier (install deps faite).
- Pendant la démo, l’IA ne génère que du code applicatif (components/styles).

## Validation
Validation minimale et stable :
- `npm run build`

Validation optionnelle (si tu veux illustrer “tests”) :
- `npm run test` (si Vitest est présent) avec 1–2 tests très simples

## Contraintes
- Éviter en live : ajout de dépendances, modifications de config, refactor massif.
- Limiter la surface de génération à 2–4 fichiers pour rapidité et fiabilité.
