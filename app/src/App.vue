<script setup lang="ts">
import Deck from './components/Deck.vue';
import FunFacts from './components/FunFacts.vue';

const demoFacts: Array<{ title: string; description: string; tag: string; confidence: string }> = [];
</script>

<template>
  <main class="app-shell baseline">
    <header>
      <p class="eyebrow">Lunch & Learn — IA comme système</p>
      <h1>État initial — avant génération</h1>
      <p class="subtitle">
        Cette version est volontairement minimale. Le contenu et le style final seront générés pendant la démo.
      </p>
    </header>

    <Deck />
    <FunFacts :items="demoFacts" />
  </main>
</template>
