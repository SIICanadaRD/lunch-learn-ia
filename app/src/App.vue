<script setup lang="ts">
import Deck from './components/Deck.vue';
import FunFacts from './components/FunFacts.vue';

// Placeholder : la valeur finale sera injectée/générée pendant la démo.
const demoWord = 'Mot à générer pendant la démo';

// Placeholder : la liste finale sera générée pendant la démo.
const demoFacts = [
  'Fun fact #1 (placeholder)',
  'Fun fact #2 (placeholder)',
  'Fun fact #3 (placeholder)',
];
</script>

<template>
  <main class="app-shell">
    <header>
      <p class="eyebrow">Lunch & Learn — IA comme système</p>
      <h1>{{ demoWord }}</h1>
      <p class="subtitle">Contenu provisoire : il sera généré en live pendant la démo.</p>
    </header>

    <Deck />
    <FunFacts :items="demoFacts" />
  </main>
</template>
