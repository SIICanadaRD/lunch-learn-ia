# Active Context — focus immédiat (atelier demain)

## Focus du moment
- Finaliser un **cas pratique démonstratif** : “prompt pauvre → résultat précis”
- Préparer les prompts / règles pour que la génération soit rapide et reproductible
- Sécuriser la démo avec un fallback

## Pendant la démo (pour que ce soit bien pris en compte)
- Inclure explicitement en contexte :
  - tout le dossier `memory-bank/`
  - tout le dossier `demo/` (contrat + prompt + validation)
- Le fichier source de vérité côté démo est : `demo/contract.md` (contraintes + fichiers autorisés).

## Cas pratique — décision
### Objectif
Générer une page web “suite des slides” à partir d’un mot reçu par email.

### Entrées
- Dernier email Gmail via MCP (subject/body)
- Contexte de l’atelier (message clé + structure du pipeline)
- Contrat de fichiers (Vue components) + contraintes

### Sortie attendue
Une webapp Vite + Vue (scaffold prêt) qui affiche :
- Le mot/objet du volontaire (en titre)
- Un mini rappel du pipeline **Objectif → Entrées → LLM → Sortie → Validation**
- Une section de **révélation animée du mot** (boîte à ouvrir + représentation CSS du mot)

### Validation
- `npm run build`

### Fallback
- Si MCP Gmail échoue : le mot est donné dans le prompt.

## Prompts de démo (squelettes)
### Prompt minimal (Plan A)
> C’est parti pour la démo.

### Prompt fallback (Plan B)
> C’est parti pour la démo. Le mot est : « <MOT> ».

### Règles (à injecter en système / instructions)
- Récupère le dernier email (ou utilise le mot fourni).
- Ne change pas la config Vite.
- Modifie uniquement les fichiers autorisés (liste fournie).
- Produit du code complet, copiable/collable.
- Assure-toi que `npm run build` passe.

## Décision récente (contrat renforcé)
- `demo/contract.md` autorise désormais, en plus des composants Vue/CSS, des fichiers TS ciblés :
  - `src/types/*.ts`
  - `src/data/*.ts`
  - `src/composables/*.ts`
- La section “Fun Facts” est remplacée par une interaction obligatoire de révélation (boîte animée + CSS art du mot).
- Le pipeline doit être plus visuel et interactif (hover/clic + panneau dynamique inputs/outputs/risques/contrôles).
