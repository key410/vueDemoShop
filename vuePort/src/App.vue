<script setup>
import Menu from "./components/Menu.vue";
import Title from "./components/Title.vue";
import MainBody from "./components/MainBody.vue";
import GoPortfolio from "./components/GoPortfolio.vue"
</script>

<template>
  <header>
    <Menu></Menu>
    <Title></Title>
  </header>

  <main>
    <MainBody></MainBody>
  </main>

  <footer>
    <GoPortfolio></GoPortfolio>
  </footer>
</template>