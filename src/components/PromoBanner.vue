<script setup lang="ts">
</script>

<template>
  <div class="promo-banner">
     <div class="promo-banner__contents">
        <h3>Lorem ipsum dolor sit amet, consectetur adipiscing elit!</h3>
        <a href="#">Call Now</a>
     </div>
  </div>
</template>

<style lang="scss" scoped>
  .promo-banner {
    align-items: center;
    width: 100%;
    margin: 0 auto 20px;
    padding: 30px 20px;
    background-color: #F56A75;

    &__contents {
        display: flex;
        flex-direction: column;
        row-gap: 20px;
        max-width: 1090px;
        margin: 0 auto;
        text-align: center;
        align-items: center;

        @media only screen and (min-width: 768px) {
            justify-content: space-between;
            text-align: left;
            flex-direction: row;
            column-gap: 20px;
        }

        h3 {
            color: #FFFFFF;
            font-size: 24px;
            line-height: 36px;
        }

        a {
            background-color: #0E3757;
            color: #FFFFFF;
            padding: 13px 0;
            font-size: 16px;
            border-radius: 4px;
            width: 290px;
            text-align: center;

            @media only screen and (min-width: 768px) {
                width: 120px;
            }
        }

    }
  }
</style>
