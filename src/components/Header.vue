<script setup lang="ts">
  import Logo from './Logo.vue'
  import Menu from './Menu.vue'
  import imgUrl from "../assets/images/brand/logo/primary.png"
</script>

<template>
  <section id="header">
    <Logo :imgUrl="imgUrl" />
    <Menu />
  </section>
</template>

<style scoped>
  #header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1087px;
    margin: 20px auto;
    padding: 0 20px;
  }
</style>
