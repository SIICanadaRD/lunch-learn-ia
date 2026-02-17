# 2. Penser l’IA comme un système

### 0:00 – 0:30 | Accroche + intention

“Avant de passer aux cas pratiques, je veux qu’on se mette d’accord sur **un modèle mental**. Si on le comprend, tout devient plus simple : pourquoi parfois ça marche super bien, pourquoi parfois c’est nul, et surtout **où agir** pour améliorer les résultats.

L’idée est dans le titre : **penser l’IA comme un système**, pas comme une personne. Un système, ça a des **entrées**, un **traitement**, des **sorties**, et des **contrôles**.”

---

### 0:30 – 1:20 | Lecture du pipeline (vue d’ensemble)

“Regardez la ligne du bas : **Objectif → Entrées → LLM → Sortie → Validation**.

- À gauche, on définit ce qu’on veut.
- Ensuite, on fournit la matière.
- Le LLM génère une proposition.
- On récupère une sortie.
- Et on valide avant d’utiliser.

Ce qui est important : dans ce schéma, la valeur ne vient pas du ‘générateur’ au milieu. Elle vient du fait qu’on **cadre** bien au début et qu’on **contrôle** bien à la fin.”

*(petite pause)*

---

### 1:20 – 2:05 | Bloc 1 — Objectif (où l’humain apporte la clarté)

“Premier bloc : **Objectif**. Ici, l’input humain, c’est ce petit cartouche : **But / Public / Format**.

C’est très concret :

- **But** : qu’est-ce qu’on cherche à obtenir ? Informer, convaincre, résumer, décider, produire un plan ?
- **Public** : un expert, un manager, un client, un nouveau dans l’équipe ?
- **Format** : mail, slide, note de synthèse, tableau comparatif, checklist, user story…

Si vous ne donnez pas ça, le modèle choisit ‘au hasard’ le style
 et le niveau de détail, donc vous aurez une réponse qui peut être 
correcte… mais **pas adaptée**.”

**Mini-exemple oral** :

“‘Explique le RAG’ → ce sera générique.

‘Explique le RAG à un directeur, en 5 bullets, sans jargon’ → d’un coup, c’est utilisable.”

---

### 2:05 – 3:05 | Bloc 2 — Entrées (où la qualité se gagne)

“Deuxième bloc : **Entrées**. Là, on met **Contexte / Docs / Exemples**.

C’est l’endroit où on gagne le plus, parce que le LLM n’est pas une mémoire de votre entreprise. Donc :

- **Contexte** : votre situation, vos contraintes, votre objectif réel.
- **Documentation** : extraits de docs, règles internes, chiffres, messages clients, spécifications.
- **Exemples** : un exemple de ‘bon rendu’ vaut souvent 10 lignes d’explications.

Une phrase importante : **si l’info n’est pas dans les entrées, le modèle peut la ‘compléter’**
 — et il le fera de façon plausible, pas forcément vraie. Donc plus on 
veut du fiable, plus on doit donner des éléments concrets.”

**Question au public (rapide)** :

“Sur vos sujets du quotidien, l’info est plutôt dans votre tête, dans des docs, ou dispersée dans des mails/Teams ?”

*(laisser 1–2 réponses, puis rebond)*

“Justement, ‘Entrées’ c’est aussi ça : rassembler le bon matériau.”

---

### 3:05 – 3:50 | Bloc 3 — LLM (le traitement : génération du plausible)

“Troisième bloc : **LLM**. Ici, je veux être précis : le LLM **génère**. Il produit une réponse cohérente selon ce qu’on lui donne.

Le cartouche au-dessus mentionne **Paramètres / RAG**. Ça sert à rappeler qu’il peut y avoir une couche ‘système’ :

- des **paramètres** (plus créatif vs plus stable),
- du **RAG** (aller chercher des passages dans vos documents pour répondre).

Mais même avec ça, l’idée reste la même : le centre du schéma, 
c’est un moteur de génération. Donc on évite de lui demander ‘la 
vérité’. On lui demande plutôt : *propose*, *structure*, *rédige*, *compare*, *met en forme*, *suggère des pistes* — et ensuite on contrôle.”

---

### 3:50 – 4:30 | Bloc 4 — Sortie (post-édition, pas livraison)

“Quatrième bloc : **Sortie**. Et là, c’est un piège classique : prendre la sortie comme un livrable final.

Le cartouche dit **Relecture / Ajustements**. Concrètement, ça veut dire :

- ajuster le ton,
- supprimer les approximations,
- compléter ce qui manque,
- et surtout aligner avec vos contraintes réelles.

La bonne posture : **la sortie est un brouillon accéléré**. L’IA fait gagner du temps sur la première version, pas sur la responsabilité.”

---

### 4:30 – 5:10 | Bloc 5 — Validation (le filet de sécurité)

“Dernier bloc : **Validation** avec **Sources / Tests / Approbation**.

Selon le cas, valider ça peut vouloir dire :

- demander des **sources** ou retrouver la source dans vos docs,
- faire un **test** (si c’est du code, une formule, un calcul),
- ou une **approbation** (si c’est un message client, un livrable, une décision).

Plus l’enjeu est élevé, plus la validation doit être forte. C’est ce qui rend le système fiable.”

---

### 5:10 – 5:30 | Conclusion + transition vers cas pratiques

“Donc, retenez une phrase : **l’humain cadre en amont et valide en aval**. Le LLM, au milieu, accélère la production, mais c’est le système autour qui garantit la qualité.

Et
 maintenant, dans les cas pratiques, on va appliquer exactement ce flux :
 objectif clair, bonnes entrées, génération, post-édition, validation.”