# Contrat de génération — Démo Vite + Vue

## Intention
À partir d’un **mot** (issu du dernier email Gmail via MCP, ou fourni en fallback), générer une page web “suite des slides” :
- Le scénario doit montrer un **avant / après** clair
- **Avant** : site placeholder (structure premium, contenu vide)
- **Après** : contenu final contextualisé au mot
- Titre = le mot
- Une section pipeline **premium et interactive** basée sur la structure du schéma (`demo/schema-pipeline.png`)
- Une section **animation de révélation** (boîte à ouvrir) qui dévoile le mot et une représentation CSS du mot
- Une section de crédibilité expliquant pourquoi le résultat est fiable (système + validation)

## Contraintes (important)
- **Ne pas installer de dépendances**
- **Ne pas modifier** la config Vite / npm scripts
- Ne pas ajouter de routing, store, etc.
- Respecter strictement les fichiers autorisés
- Design moderne, lisible, responsive (desktop + mobile)
- Après génération: pas de placeholders (“lorem ipsum”, “à compléter”, etc.)
- Privilégier une architecture claire : séparation composant / données / logique TS quand pertinent

## Exigence de scénario démo
- Conserver dans le repo une version “avant” (placeholders)
- La version “avant” doit rester **quasi brute** (HTML simple + CSS minimal)
- Lors du prompt de démo, remplacer complètement les placeholders par le contenu final
- Lors du prompt de démo, générer **aussi** le design final (layout + styles + interactions)
- Le diff avant/après doit être évident à montrer

## Exigences UI/UX minimales
- Hero section claire (mot + sous-titre narratif)
- Pipeline en 5 briques : **Objectif → Entrées → LLM → Sortie → Validation**
- Interaction obligatoire : hover **et/ou** clic sur une brique => focus visuel + panneau de détails unique qui change
- Micro-interactions CSS (hover, active, transition)
- Densité de contenu suffisante (pas juste 2-3 lignes globales)
- Hiérarchie visuelle soignée (cartes, contrastes, spacing)

## Exigence pipeline — version épurée (obligatoire)
Le pipeline doit être **simple, lisible, non répétitif**.

### Structure attendue
- 5 briques uniquement : **Objectif → Entrées → LLM → Sortie → Validation**
- Chaque brique contient un libellé court + **1 phrase max**
- Un **seul panneau dynamique** de détail (pas plusieurs sous-cartes répétitives)

### Interaction attendue
- Clic ou hover sur une brique => état actif clairement visible
- Le panneau dynamique doit afficher, dans cet ordre :
  1. **Inputs humains** (ce qui alimente l’étape)
  2. **Traitement machine** (ce que fait le système/LLM)
  3. **Livrable** (ce qui est produit à cette étape)

### Contraintes de lisibilité
- Maximum **3 à 4 inputs humains** par étape
- Labels courts et concrets (éviter le jargon inutile)
- Interdiction de dupliquer le même contenu dans plusieurs zones

### Interdictions explicites
- Pas de grille multi-cartes redondantes de type : inputs/outputs/risques/contrôles
- Pas de bloc texte long par étape
- Pas de pipeline purement décoratif sans lien clair avec l’action humaine

### Critères d’acceptation pipeline
Le pipeline est valide seulement si :
- la part humaine est immédiatement visible au clic sur une brique,
- la section est compréhensible en < 10 secondes,
- le contenu est concis et non répétitif,
- la narration "**IA = système**" est perceptible (humain alimente, machine exécute, livrable contrôlé).

## Section “Révélation du mot” (obligatoire, remplace Fun Facts)
La page doit contenir une expérience interactive de révélation :

1) **Boîte fermée (état initial)**
- Une boîte/coffre/containment visuel est affichée fermée.
- Le design de la boîte doit être cohérent avec le mot.

2) **Interaction d’ouverture**
- L’utilisateur peut ouvrir la boîte (clic au minimum).
- Animation fluide (ouverture + apparition du contenu).
- La séquence est rejouable (bouton reset/replay ou interaction équivalente).

3) **Révélation visuelle du mot**
- Le mot apparaît avec une animation de révélation.
- Une **représentation du mot en pur CSS** apparaît (formes, gradients, pseudo-éléments, etc.).
- Cette représentation ne doit pas dépendre d’images externes.

4) **Accessibilité minimale**
- Interaction utilisable au clavier (focus visible, Enter/Espace).
- Contrastes lisibles et animations non bloquantes.

## Design piloté par le mot (obligatoire)
Le design final doit être **guidé par le mot** reçu (et pas seulement affiché dans le titre).

### 1) Interprétation explicite du mot
- Déduire une direction artistique à partir du mot :
  - ambiance (ex: énergétique, apaisante, premium, futuriste, naturelle)
  - registre visuel (ex: tech, organique, industriel, éditorial)
  - niveau d’intensité (sobre, équilibré, expressif)
- Si le mot est ambigu, choisir une interprétation cohérente et l’assumer.

### 2) Tokens de design dérivés du mot
Le rendu doit inclure des choix visuels cohérents entre eux :
- palette (3 à 5 couleurs) alignée avec le mot
- style des surfaces (cartes, bordures, ombres, flou, texture légère si utile)
- rythme visuel (densité, spacing, contrastes)
- style d’animations/micro-interactions (fluide, dynamique, discret, etc.)

Interdiction : livrer un thème générique qui pourrait convenir à n’importe quel mot.

### 3) Traduction visuelle dans toutes les sections
La direction artistique liée au mot doit se retrouver dans :
- Hero
- Pipeline interactif
- Révélation animée du mot (boîte + CSS art)
- Bloc crédibilité

Chaque section doit participer au même “univers” visuel (cohérence globale).

### 4) Justification design dans la réponse
En plus du code, fournir 4 à 6 puces :
- “Pourquoi ce design correspond au mot”
- chaque puce doit relier un choix concret (couleurs, typo, animations, structure) au mot.

### 5) Critères d’acceptation design
Le résultat est valide seulement si :
- sans lire le titre, la direction artistique évoque déjà le mot
- au moins 3 choix visuels majeurs sont clairement reliés au mot
- le rendu reste lisible et responsive (desktop + mobile)

## Fichiers autorisés
L’IA ne doit modifier/créer **que** ces fichiers :
- `src/App.vue`
- `src/components/Deck.vue`
- `src/components/RevealBox.vue`
- `src/style.css`

Fichiers TypeScript désormais autorisés (optionnels mais recommandés) :
- `src/types/*.ts`
- `src/data/*.ts`
- `src/composables/*.ts`

Remarque : l’IA peut supprimer l’usage de `FunFacts.vue` si remplacé par `RevealBox.vue`.

Tout le reste est **interdit**.

## Attendu dans la réponse
- Une liste des fichiers modifiés
- Le contenu complet de chaque fichier (pour copier/coller)
- Une courte checklist de validation technique + UX
- 3–5 puces “choix d’architecture” (ex: pourquoi extraire la logique en TS/composable)
