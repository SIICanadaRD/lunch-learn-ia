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

## À faire (court terme — avant l’atelier)
- Mettre en place le scaffold Vite+Vue (si pas déjà fait)
- Définir le contrat de fichiers exact pour la génération (2–4 fichiers)
- Préparer 1 exécution “à blanc” (output de référence) en cas de souci live
- (Optionnel) ajouter 1 commande de validation : `npm run build` (+ tests si présents)

## Risques connus
- Dépendance réseau / OAuth / MCP pendant la démo → prévoir fallback prompt
- Dépendance temps : limiter la génération à peu de fichiers
