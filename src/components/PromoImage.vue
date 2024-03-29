<script setup lang="ts">
    defineProps<{ imgUrl: string }>()
    import imgUrl from "../assets/images/brand/browser-image.png"
</script>

<template>
    <div id="promo-image">
        <img :src="imgUrl" alt="Site logo">
    </div>
</template>

<style lang="scss" scoped>
  #promo-image {
    display: block;
    max-width: 914px;
    margin: 0 auto;

    @media only screen and (min-width: 768px) {
        margin-top: 80px;
    }

    img {
        width: 100%;
        height: auto;

        // @media only screen and (min-width: 768px) {
        //     width: 120px;
        //     height: 50px;
        // }
    }
  }
</style>
