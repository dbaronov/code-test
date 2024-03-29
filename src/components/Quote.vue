<script setup lang="ts">
</script>

<template>
    <div class="blockquote">
        <div class="blockquote__content">
            <blockquote cite="">
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
            </blockquote>
            <span class="blockquote__icon">
                <img src="../assets/images/brand/icon/quotes.png" alt="Quote icon">
            </span>
            <p>Roy Barber - Dotcentric</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
  .blockquote {
    display: flex;
    row-gap: 30px;
    flex-direction: column;
    border-top: 1px solid #EEEEEE;
    border-bottom: 1px solid #EEEEEE;
    // justify-content: space-around;
    max-width: 1087px;
    margin: 40px auto;
    padding: 60px 15px;

    @media only screen and (min-width: 768px) {
        flex-direction: row;
        column-gap: 30px;
        justify-content: center;
        margin: 100px auto;
    }

    &__content {
        position: relative;
        padding-left: 50px;
    }

    &__icon {
        position: absolute;
        left: 0;
        top: 10px;
        max-width: 1090px;
    }
    
    blockquote {
        font-size: 24px;
        line-height: 36px;
        color: #0E3757;
        margin-bottom: 10px;

        @media only screen and (min-width: 768px) {
            font-size: 28px;
            line-height: 42px;
            max-width: 812px;
            margin-bottom: 20px;
        }
    }

    p {
        font-size: 18px;
        line-height: 30px;
        color: #8D9CA8;
    }
  }
</style>