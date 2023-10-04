<!-- ./layouts/default.vue -->
<script setup>
const { $pwa } = useNuxtApp();
</script>
<template>
  <main>
    <slot />
    <div v-show="$pwa?.needRefresh">
      <span> New content available, click on reload button to update. </span>

      <button @click="$pwa.updateServiceWorker()">Reload</button>
    </div>
  </main>
</template>
