<script setup lang="ts">
interface Props {
  items: string[];
}

defineProps<Props>();
</script>

<template>
  <section class="card">
    <h2 class="card-title">Fun facts (placeholder)</h2>
    <p class="card-lead">Cette section sera générée en live pendant la démo.</p>

    <ul class="fun-facts">
      <li v-for="(item, index) in items" :key="index">
        {{ item }}
      </li>
    </ul>
  </section>
</template>
