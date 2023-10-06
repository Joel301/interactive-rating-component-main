<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <section class="mainContainer">
    <RouterView />
  </section>
</template>

<style scoped>
.mainContainer {
  background-color: var(--Dark-Blue);
  color: antiquewhite;
  border-radius: 2em;
  width: calc(375px - 1.3em - 5rem);
  display: flex;
  margin: 2rem;
  padding: 1.3em;

}
</style>
