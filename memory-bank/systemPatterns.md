# System Patterns — conventions et patterns à réutiliser

## Pattern 1 — Pipeline “Système IA”
Le repo et la démo suivent une structure stable :

1) **Objectif**
   - But / public / format / contraintes / critères de réussite
2) **Entrées**
   - Contexte + extraits de doc + exemples + contraintes
3) **Génération (LLM)**
   - Produire une proposition conforme à un contrat (format attendu)
4) **Post-édition**
   - Ajuster, factoriser, clarifier
5) **Validation**
   - Build/tests/checklist (selon enjeu)

## Pattern 2 — Contrat de sortie (anti-blabla)
Pour éviter les réponses inutilisables, demander des sorties “fichiers” :

- Lister les **fichiers à créer/modifier**
- Donner le **contenu complet** de chaque fichier
- Respecter une structure de projet existante

Exemple de contrat (cas pratique Vite+Vue) :
- Édite uniquement :
  - `src/App.vue`
  - `src/components/Deck.vue`
  - `src/components/RevealBox.vue`
  - `src/style.css` (ou styles scoped)
- Peut aussi créer des fichiers TS ciblés si autorisé :
  - `src/types/*.ts`
  - `src/data/*.ts`
  - `src/composables/*.ts`
- Ne pas ajouter de dépendances.
- Ne pas modifier la config Vite.

## Pattern 3 — Guardrails (fiabilité)
Règles recommandées à injecter (prompts / instructions) :
- Si une info manque : **poser une question** plutôt qu’inventer.
- Indiquer les hypothèses explicitement.
- Proposer une checklist de validation.
- Pour le code : garantir que `npm run build` passe.

## Pattern 4 — Fallbacks (robustesse démo)
Tout outil externe peut tomber (auth, réseau).
Donc :
- Plan A : outil MCP (Gmail)
- Plan B : entrée manuelle (mot fourni dans le prompt)
