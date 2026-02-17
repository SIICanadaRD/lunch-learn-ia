# Product Context — pourquoi et comment ça doit “marcher”

## Pourquoi ce projet existe
Cet atelier vise à corriger un modèle mental courant : *« l’IA est un outil / une boîte magique »*.
Le message central est : **l’IA est un composant au sein d’un système**.

## Problème que l’on résout
Les usages “prompt isolé” donnent souvent :
- des réponses génériques
- de l’incohérence entre itérations
- des erreurs/hallucinations non détectées
- peu de reproductibilité (impossible de refaire pareil demain)

## Expérience attendue (ce que le public doit ressentir)
1) *« OK, je comprends pourquoi mon prompt parfois marche et parfois non »*
2) *« Je sais où agir : objectif, entrées, format, validation »*
3) *« Je peux transformer un usage ponctuel en mini-workflow »*

## Messages clés (à marteler)
- **Qualité = Contexte + Consignes + Vérifications**
- Le LLM produit du **plausible**, pas de la vérité.
- L’humain **cadre** en amont et **valide** en aval.
- Un bon setup (règles + contexte + outils + validation) rend les résultats :
  - plus **fiables**
  - plus **cohérents**
  - plus **reproductibles**

## Cas pratique : ce qu’il doit démontrer
- Prompt pauvre → output précis grâce au système (Memory Bank + règles)
- Outils (MCP) = capacité d’action (lire une mailbox), pas juste génération
- Validation intégrée = passage du “wow” à quelque chose d’adoptable en entreprise
