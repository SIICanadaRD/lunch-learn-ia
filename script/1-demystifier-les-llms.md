# 1. Démystier les LLMs

## Démystifier les LLMs

### 0:00 – 0:30 | Accroche

“Avant de parler d’usages, on va **démystifier les LLMs**. L’objectif, ce n’est pas de rentrer dans la technique, c’est d’avoir le bon réflexe : savoir **ce qu’on peut attendre** d’un LLM, et **où sont les pièges**.”

---

### 0:30 – 2:15 | Ce que c’est ✅ (côté gauche)

**1) “Un modèle de langage”**

“Un LLM, c’est d’abord un **modèle de langage** : il **prédit la suite des mots**.
 Ça paraît simpliste, mais c’est essentiel : il optimise la probabilité 
d’une réponse plausible dans le langage, pas la ‘vérité’.”

**2) “Un moteur de complétion”**

“Donc c’est un **moteur de complétion**. Il est très fort pour :

- reformuler,
- structurer,
- résumer,
- générer des variantes,
- proposer un plan,
- écrire un mail, une note, un script, une checklist.

Mais retenez la phrase : il propose des formulations **plausibles**, pas des faits.”

**3) “Un outil sensible au contexte”**

“Troisième point : il est **sensible au contexte**. Sa 
‘compréhension’ dépend de ce qu’on lui donne : si le contexte est 
pauvre, la réponse sera générique ; si le contexte est précis, la 
réponse devient utile. C’est pour ça qu’on insiste autant sur les 
entrées : contraintes, exemples, documents.”

**4) “Un générateur”**

“Enfin, c’est un **générateur** : il produit un résultat selon des **consignes**. Plus vos consignes sont claires (format, ton, étapes, critères), plus vous pilotez le résultat.”

*(transition)* “Donc côté gauche : langage, complétion, contexte, consignes. Maintenant, les confusions classiques.”

---

### 2:15 – 4:20 | Ce que ce n’est pas ❌ (côté droit)

**1) “Une source de vérité”**

“Un LLM n’est pas une **source de vérité**. Il peut **inventer**
 des informations : on appelle ça des hallucinations. Ce n’est pas rare,
 et ce n’est pas un bug ‘exceptionnel’ : c’est une conséquence logique 
du fait qu’il génère du plausible.”

**2) “Un expert métier”**

“Ce n’est pas non plus un **expert de votre métier**. Il ne
 connaît pas vos règles internes, vos données à jour, vos process, vos 
exceptions. Il peut connaître des généralités, mais il ne connaît pas *votre* contexte tant que vous ne le fournissez pas.”

**3) “Une mémoire”**

“Troisième point : ce n’est pas une **mémoire**. Il est 
‘amnésique’ au sens où, d’une session à l’autre, il ne retient pas comme
 un collègue qui capitalise. Donc si vous voulez de la cohérence, il 
faut **réinjecter** le contexte utile, ou s’appuyer sur des mécanismes type documents/RAG quand ils existent.”

**4) “Un responsable”**

“Et enfin, ce n’est pas un **responsable**. La 
responsabilité, c’est nous : c’est vous qui décidez si vous utilisez la 
réponse, si vous la modifiez, si vous la validez. L’IA peut aider, mais 
elle ne ‘signe’ pas.”

---

### 4:20 – 5:00 | Conclusion (la formule en bas) + transition

“Tout ça mène à la formule en bas : **Qualité = contexte + consignes + vérifications**.

- **Contexte** : ce que je lui donne pour éviter le générique et limiter l’invention.
- **Consignes** : comment je veux la sortie (format, contraintes, critères).
- **Vérifications** : ce qui rend le résultat utilisable et sûr (sources, tests, relecture).

Et c’est exactement ce qu’on va formaliser juste après avec la slide suivante : **penser l’IA comme un système** — avec des entrées, un générateur au milieu, et une validation humaine.”