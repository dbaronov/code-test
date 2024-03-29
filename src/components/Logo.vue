<script setup lang="ts">
    defineProps<{ imgUrl: string }>()
    // import imgUrl from "../assets/images/brand/logo/primary.png"
</script>

<template>
    <div id="logo">
        <img :src="imgUrl" alt="Site logo">
    </div>
</template>

<style lang="scss" scoped>
  #logo {
    display: flex;
    max-width: 1087px;

    img {
        width: 76px;
        height: 32px;

        @media only screen and (min-width: 768px) {
            width: 120px;
            height: 50px;
        }
    }
  }
</style>
