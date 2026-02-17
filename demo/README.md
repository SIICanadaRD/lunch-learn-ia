# Demo — Cas pratique "prompt pauvre → résultat précis"

Ce dossier contient les **assets de démo** à inclure en contexte lors de la génération.

## But
À partir d’un prompt minimal (ex: « C’est parti pour la démo. »), l’agent doit :
1) Récupérer un mot depuis Gmail via MCP (ou fallback : mot fourni dans le prompt)
2) Générer une mini webapp **Vite + Vue** (scaffold déjà prêt)
3) Valider via `npm run build`

## Fichiers
- `demo/contract.md` : contrat de génération (fichiers autorisés, contraintes)
- `demo/prompt.md` : prompt “prêt à coller” (plan A + fallback)
- `demo/validation.md` : checklist de validation + commandes

## Important (pendant la démo)
- Mets **tout ce dossier `demo/` en contexte** dans l’agent.
- Si le MCP Gmail échoue : utilise le prompt fallback et continue.
