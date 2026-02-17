# Contrat de génération — Démo Vite + Vue

## Intention
À partir d’un **mot** (issu du dernier email Gmail via MCP, ou fourni en fallback), générer une page web “suite des slides” :
- Titre = le mot
- Une section qui explique le pipeline **Objectif → Entrées → LLM → Sortie → Validation**
- Une section “fun” (2–5 fun facts / analogies) liée au mot

## Contraintes (important)
- **Ne pas installer de dépendances**
- **Ne pas modifier** la config Vite / npm scripts
- Ne pas ajouter de routing, store, etc.
- Code simple, lisible, copiable

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
- Une courte checklist de validation
