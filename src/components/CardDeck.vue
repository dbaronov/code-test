<script setup lang="ts">
    defineProps<{ imgUrl: string }>()
    import imgUrl from "../assets/images/brand/icon/service-badge.png"
    const services = await fetch(`http://localhost:5173/api`).then((response) => response.json())
    // See vite.config.ts for proxy settings
</script>

<template>
    <div class="card-deck">
        <div class="card-deck__item" v-for="(service, index) in services" :key="index">
            <div class="card-deck__image-wrap">
                <img :src="imgUrl" alt="Card image">
                <span>{{index + 1}}</span> <!-- Image URL is not complete in JSON response -->
            </div>
            <h4>{{service.name}}</h4>
            <p>{{service.description}}</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
  .card-deck {
    display: flex;
    row-gap: 30px;
    flex-direction: column;
    justify-content: space-around;
    max-width: 1087px;
    margin: 0 auto;
    padding: 0 15px;

    @media only screen and (min-width: 768px) {
        flex-direction: row;
        column-gap: 30px;
    }
    
    h4 {
        font-size: 24px;
        line-height: 36px;
        text-align: center;
        color: #0E3757;
        margin-bottom: 10px;

        @media only screen and (min-width: 768px) {
            font-size: 28px;
            line-height: 42px;
        }
    }

    p {
        font-size: 20px;
        line-height: 30px;
        text-align: center;
        color: #8D9CA8;
    }

    &__image-wrap {
        display: table;
        margin: 0 auto;
        position: relative;

        span {
            position: absolute;
            top: 0;
            right: 0;
            background-color: #F56A75;
            width: 39px;
            height: 39px;
            line-height: 39px;
            color: #FFFFFF;
            text-align: center;
            border-radius: 20px;
        }

        img {
            width: 150px;
            height: 150px;
            margin: 0 auto;
            margin-bottom: 10px;
        }
    }
  }
</style>
