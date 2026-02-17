<script setup lang="ts">
import { computed, ref } from 'vue';

type StepId = 'objectif' | 'entrees' | 'llm' | 'sortie' | 'validation';

interface PipelineStep {
  id: StepId;
  title: string;
  summary: string;
  inputs: string[];
  outputs: string[];
  risks: string[];
  controls: string[];
}

const steps: PipelineStep[] = [
  {
    id: 'objectif',
    title: 'Objectif',
    summary: 'Placeholder: objectif final à injecter après réception du mot.',
    inputs: ['À définir pendant la génération'],
    outputs: ['À définir pendant la génération'],
    risks: ['À définir pendant la génération'],
    controls: ['À définir pendant la génération'],
  },
  {
    id: 'entrees',
    title: 'Entrées',
    summary: 'Placeholder: sources et contraintes à compléter après le prompt.',
    inputs: ['À définir pendant la génération'],
    outputs: ['À définir pendant la génération'],
    risks: ['À définir pendant la génération'],
    controls: ['À définir pendant la génération'],
  },
  {
    id: 'llm',
    title: 'LLM',
    summary: 'Placeholder: logique de génération en attente.',
    inputs: ['À définir pendant la génération'],
    outputs: ['À définir pendant la génération'],
    risks: ['À définir pendant la génération'],
    controls: ['À définir pendant la génération'],
  },
  {
    id: 'sortie',
    title: 'Sortie',
    summary: 'Placeholder: structure de sortie en attente de contenu final.',
    inputs: ['À définir pendant la génération'],
    outputs: ['À définir pendant la génération'],
    risks: ['À définir pendant la génération'],
    controls: ['À définir pendant la génération'],
  },
  {
    id: 'validation',
    title: 'Validation',
    summary: 'Placeholder: validation finale à injecter après génération.',
    inputs: ['À définir pendant la génération'],
    outputs: ['À définir pendant la génération'],
    risks: ['À définir pendant la génération'],
    controls: ['À définir pendant la génération'],
  },
];

const activeStepId = ref<StepId>('objectif');

const activeStep = computed(() => {
  return steps.find((step) => step.id === activeStepId.value) ?? steps[0];
});
</script>

<template>
  <section>
    <h2>Pipeline (placeholder)</h2>
    <p>Le pipeline interactif final sera généré pendant la démo.</p>

    <div class="pipeline-premium" role="tablist" aria-label="Pipeline placeholder">
      <button
        v-for="(step, index) in steps"
        :key="step.id"
        class="pipeline-node simple"
        role="tab"
        :aria-selected="activeStepId === step.id"
        @click="activeStepId = step.id"
      >
        {{ index + 1 }}. {{ step.title }}
      </button>
    </div>

    <p class="pipeline-note">Étape sélectionnée : {{ activeStep.title }} — {{ activeStep.summary }}</p>
  </section>
</template>
