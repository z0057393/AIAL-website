<template>
  <button :class="{ primary }" class="base-button">
    {{ label }}
  </button>
</template>

<script setup lang="ts">
defineProps<{
  label: string;
  primary?: boolean;
}>();
</script>

<style scoped>
.base-button {
  padding: 0.5em 1em;
  font-size: 1rem;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.base-button.primary {
  background-color: #1e90ff;
  color: white;
}

.base-button:not(.primary) {
  background-color: #f0f0f0;
  color: #333;
}
</style>
