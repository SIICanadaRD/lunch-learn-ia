# Progress — état du repo

## Ce qui existe
- Scripts Markdown :
  - `script/1 Démystifier les LLMs …` (partie 1)
  - `script/2 Penser l’IA comme un système …` (partie 2)
  - `script/Lunch&Learn script …` (intro + structure)

## Ce qui fonctionne déjà
- Narration claire sur :
  - ce qu’est un LLM / limites
  - pipeline “objectif→entrées→LLM→sortie→validation”
  - posture : cadrage + validation
- Contrat de démo renforcé (design piloté par le mot + interactions imposées)
- Prompt de démo aligné avec le nouveau contrat

## À faire (court terme — avant l’atelier)
- Mettre en place le scaffold Vite+Vue (si pas déjà fait)
- Préparer 1 exécution “à blanc” (output de référence) en cas de souci live sur la nouvelle version de contrat
- (Optionnel) ajouter 1 commande de validation : `npm run build` (+ tests si présents)

## Décision appliquée
- Les changements de code de test (thème papillon) ont été annulés volontairement.
- Seules les évolutions de la couche “système” sont conservées :
  - `demo/contract.md`
  - `demo/prompt.md`
  - mise à jour des fichiers Memory Bank correspondants.

## Risques connus
- Dépendance réseau / OAuth / MCP pendant la démo → prévoir fallback prompt
- Dépendance temps : limiter la génération à peu de fichiers
