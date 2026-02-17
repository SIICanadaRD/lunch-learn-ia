# Validation — checklist & commandes

## Objectif
Montrer la partie **Validation** du système : on ne “livre” pas une génération non vérifiée.

## Checklist rapide
- [ ] AVANT : le site est en mode placeholder (mot en attente + contenu vide/skeleton)
- [ ] APRÈS : le mot reçu remplace l’état d’attente
- [ ] APRÈS : le CSS est significativement enrichi (layout, couleurs, interactions)
- [ ] Le titre affiche exactement le mot
- [ ] La page contient le pipeline complet (Objectif → Entrées → LLM → Sortie → Validation)
- [ ] Le pipeline est **interactif** (clic sur une brique => détails mis à jour)
- [ ] Les détails de pipeline incluent au moins : inputs, outputs, risques, contrôles
- [ ] La page contient une section “insights / fun facts” riche (cartes structurées)
- [ ] La page contient une section de crédibilité (pourquoi le résultat est fiable)
- [ ] Aucune section ne contient de placeholder
- [ ] Le design est lisible sur desktop et mobile
- [ ] Le code compile (build OK)
- [ ] Le différentiel visuel avant/après est évident en démo

## Commande minimale
Dans le projet Vite/Vue :

```bash
npm run build
```

## Optionnel (si tests en place)
```bash
npm run test
```

## Critère de réussite démo
Le public doit percevoir que le résultat provient d’un **système maîtrisé** (contexte + instructions + validation),
et pas seulement d’un texte généré rapidement.
