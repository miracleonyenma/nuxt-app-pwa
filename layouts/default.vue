<!-- ./layouts/default.vue -->
<script setup>
const { $pwa } = useNuxtApp();
</script>
<template>
  <header>
    <h1>My App</h1>
    <nav>
      <ul>
        <li>
          <NuxtLink to="/">Home</NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about">About</NuxtLink>
        </li>
      </ul>
    </nav>
  </header>
  <main>
    <slot />
    <div v-show="$pwa?.needRefresh">
      <span> New content available, click on reload button to update. </span>

      <button @click="$pwa.updateServiceWorker()">Reload</button>
    </div>
  </main>
</template>
