# Contrat de génération — Démo Vite + Vue

## Intention
À partir d’un **mot** (issu du dernier email Gmail via MCP, ou fourni en fallback), générer une page web “suite des slides” :
- Le scénario doit montrer un **avant / après** clair
- **Avant** : site placeholder (structure premium, contenu vide)
- **Après** : contenu final contextualisé au mot
- Titre = le mot
- Une section pipeline **premium et interactive** basée sur la structure du schéma (`demo/schema-pipeline.png`)
- Une section “insights / fun facts” riche et contextualisée au mot
- Une section de crédibilité expliquant pourquoi le résultat est fiable (système + validation)

## Contraintes (important)
- **Ne pas installer de dépendances**
- **Ne pas modifier** la config Vite / npm scripts
- Ne pas ajouter de routing, store, etc.
- Respecter strictement les fichiers autorisés
- Design moderne, lisible, responsive (desktop + mobile)
- Après génération: pas de placeholders (“lorem ipsum”, “à compléter”, etc.)

## Exigence de scénario démo
- Conserver dans le repo une version “avant” (placeholders)
- La version “avant” doit rester **quasi brute** (HTML simple + CSS minimal)
- Lors du prompt de démo, remplacer complètement les placeholders par le contenu final
- Lors du prompt de démo, générer **aussi** le design final (layout + styles + interactions)
- Le diff avant/après doit être évident à montrer

## Exigences UI/UX minimales
- Hero section claire (mot + sous-titre narratif)
- Pipeline en 5 briques : **Objectif → Entrées → LLM → Sortie → Validation**
- Interaction obligatoire : clic sur une brique => panneau de détails qui change (inputs/outputs/risques/contrôles)
- Micro-interactions CSS (hover, active, transition)
- Densité de contenu suffisante (pas juste 2-3 lignes globales)
- Hiérarchie visuelle soignée (cartes, contrastes, spacing)

## Fichiers autorisés
L’IA ne doit modifier/créer **que** ces fichiers :
- `src/App.vue`
- `src/components/Deck.vue`
- `src/components/FunFacts.vue`
- `src/style.css`

Tout le reste est **interdit**.

## Attendu dans la réponse
- Une liste des fichiers modifiés
- Le contenu complet de chaque fichier (pour copier/coller)
- Une courte checklist de validation technique + UX
