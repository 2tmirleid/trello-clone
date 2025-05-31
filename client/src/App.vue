<script setup>

import Sidebar from "@/components/Sidebar.vue";
</script>

<template>
  <main id="app">
      <Sidebar/>
  </main>
</template>

<style scoped>
@media screen and (min-width: 1200px) {
  #app {
    max-width: 1550px;
  }

  main {
    overflow-y: hidden;
    height: calc(100vh - 2px);
    margin: 0 auto;
    background-color: #FAFAFA;
    border: 1px solid rgba(0, 0, 0, 0.1);
    border-radius: 10px;
  }
}

@media screen and (max-width: 1200px) {
  #app {
    display: none;
  }
}
</style>
