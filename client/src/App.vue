<script setup>

import Sidebar from "@/components/Sidebar.vue";
import Header from "@/components/Header.vue";
</script>

<template>
  <main id="app">
    <Header/>
    <Sidebar/>
  </main>
</template>

<style scoped>
@media screen and (min-width: 1200px) {
  #app {
    max-width: 1550px;
  }

  main {
    display: grid;
    grid-template-columns: 225px 1fr;
    grid-template-rows: auto 1fr;
    height: calc(100vh - 2px);
    margin: 0 auto;
    background-color: #FFFFFF;
    border: 1px solid rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    overflow: hidden;
  }

  Header {
    grid-column: 2;
    grid-row: 1;
  }

  Sidebar {
    grid-column: 1;
    grid-row: 1 / span 2;
  }
}

@media screen and (max-width: 1200px) {
  #app {
    display: none;
  }
}
</style>
