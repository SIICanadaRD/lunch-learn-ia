# Validation — checklist & commandes

## Objectif
Montrer la partie **Validation** du système : on ne “livre” pas une génération non vérifiée.

## Checklist rapide
- [ ] Le titre affiche exactement le mot
- [ ] La page contient le pipeline (Objectif → Entrées → LLM → Sortie → Validation)
- [ ] La page contient une section “fun” (2–5 items)
- [ ] Le code compile (build OK)

## Commande minimale
Dans le projet Vite/Vue :

```bash
npm run build
```

## Optionnel (si tests en place)
```bash
npm run test
```
