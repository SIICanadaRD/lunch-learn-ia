# Prompt — prêt à coller (Plan A + Fallback)

## Plan A (prompt minimal)
> C’est parti pour la démo.

### Instructions implicites attendues (via contexte)
- Lire le dernier email Gmail via MCP
- Extraire le mot/objet
- Générer la webapp selon `demo/contract.md`
- Expliquer brièvement comment valider via `demo/validation.md`

## Renforcement attendu (qualité premium)
En plus des consignes de base, l’agent doit produire un résultat **ambitieux** :
- Design premium (hiérarchie visuelle, contraste, layout moderne)
- Contenu concret (pas de placeholder)
- Pipeline interactif en 5 briques (hover/clic => détails dynamiques)
- Respect de la structure du schéma `demo/schema-pipeline.png` avec un style modernisé
- Section de révélation animée : boîte à ouvrir, mot révélé, représentation CSS du mot
- Architecture plus robuste avec fichiers TypeScript autorisés (`types`, `data`, `composables`) si pertinent
- Réponse orientée livraison : fichiers complets + mini-checklist UX/tech

## Consigne de transformation (avant / après)
- Tu pars d’un état initial placeholder (site presque vide mais premium en structure)
- Tu pars d’un état initial placeholder **très simple** (contenu minimal + CSS basique)
- Tu fournis une version "après" entièrement remplie selon le mot reçu
- Tu remplaces explicitement les placeholders dans les 4 fichiers autorisés
- Tu transformes fortement le style (pas juste remplacement de texte)

## Consigne section mot (obligatoire)
- Ne génère pas une section “fun facts” générique.
- Génère une interaction “boîte à révélation” :
  - état fermé,
  - ouverture animée,
  - mot révélé,
  - représentation visuelle du mot en CSS.

## Fallback (si MCP Gmail échoue)
> C’est parti pour la démo. Le mot est : « <MOT> ».

## Rappel important
Tu dois **respecter strictement** `demo/contract.md`.
