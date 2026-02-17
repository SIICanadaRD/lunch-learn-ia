<script setup lang="ts">
interface FactItem {
  title: string;
  description: string;
  tag: string;
  confidence: 'Élevée' | 'Moyenne' | 'Faible' | string;
}

interface Props {
  items: FactItem[];
}

defineProps<Props>();
</script>

<template>
  <section>
    <h2>Insights (placeholder)</h2>
    <p>Section vide avant génération. Nombre d’items actuel : {{ items.length }}.</p>
  </section>
</template>
