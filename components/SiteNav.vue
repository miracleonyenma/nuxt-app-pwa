<script setup lang="ts">
const links = ref([
  {
    name: "Home",
    url: "/",
  },
  {
    name: "About",
    url: "/about",
  },
]);
</script>
<template>
  <nav class="site-nav">
    <ul class="links">
      <li v-for="link in links" :key="link.name" class="links__item">
        <NuxtLink :to="link.url" class="links__link">
          {{ link.name }}
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>
<style scoped>
.links {
  @apply flex items-center gap-4;
}
</style>
