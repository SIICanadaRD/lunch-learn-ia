# Project Brief — lunch&learn-ia

## Pitch
Repo de préparation d’un atelier Lunch&Learn (SII Canada) : **« L’IA n’est pas un outil, c’est un système »**.

L’objectif du repo est de **capitaliser un contexte structuré** (Memory Bank + règles) afin de pouvoir, pendant la démo, partir d’un prompt minimal et obtenir des sorties **cohérentes, fiables, reproductibles**.

## Public cible
- Employés de SII Canada (ESN)
- Majoritairement ingénieurs aéronautiques et développeurs
- Niveau IA hétérogène (débutant → avancé)

## Format et timing
- Durée totale : **30 min**
  - ~15 min : slides / narration (parties 1 & 2)
  - ~15 min : **cas pratique**

## Contenu prévu (haut niveau)
1) **Démystifier les LLMs**
   - Un LLM : modèle de langage (complétion), sensible au contexte
   - Limites : pas source de vérité, pas mémoire, pas responsable
   - Formule : **Qualité = Contexte + Consignes + Vérifications**

2) **Penser l’IA comme un système**
   - Pipeline : **Objectif → Entrées → LLM → Sortie → Validation**
   - La valeur vient du cadrage (amont) et du contrôle (aval)

3) **Cas pratique (démo live) : prompt pauvre → résultat précis**
   - Démontrer que le *système* autour (contexte, règles, outils) est la clé.

## Cas pratique (défini)
### Intention
Montrer qu’un prompt minimal (ex: « c’est parti pour la démo ») suffit si :
- le contexte est externalisé (Memory Bank)
- des règles de génération existent (contrat de fichiers, checklists)
- l’agent a des outils (MCP Gmail)
- la validation est intégrée (build/tests)

### Scénario
1) Un volontaire envoie un mail sur une **Gmail perso** avec un mot/objet.
2) L’agent récupère le dernier mail via **MCP Gmail**.
3) L’agent génère le code d’une petite webapp **Vite + Vue** (scaffold préparé en amont).
4) Validation rapide : au minimum `npm run build`.
5) Fallback : si MCP échoue, le mot est fourni dans le prompt.

## Contraintes
- Démo robuste : prévoir fallback si MCP indisponible
- Pas de données sensibles : l’email ne contient qu’un mot/objet
- Le code généré doit être **minimal** (peu de fichiers) et **testable**

## Critères de réussite
- Le message *« l’IA = système »* est compris :
  - répétabilité
  - contrôle qualité
  - cohérence des sorties
- La démo produit une page “suite des slides” pertinente en < 15 min
