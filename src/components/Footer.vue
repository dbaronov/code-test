<script setup lang="ts">
    import Logo from './Logo.vue'
    defineProps<{ imgUrl: string }>()
    import imgUrl from "../assets/images/brand/logo/secondary.png"
</script>

<template>
  <div class="footer-styled">
     <div class="footer-styled__contents">
        <p>&copy; 2021 <a href="#">Dotcentric</a> Code Test - All rights reserved - Call 01234 432 123</p>
        <Logo :imgUrl="imgUrl" />
     </div>
  </div>
</template>

<style lang="scss" scoped>
.footer-styled {
    align-items: center;
    width: 100%;
    margin: 0 auto;
    padding: 30px 20px;
    background-color: #0E3757;

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

            p {
                color: #FFFFFF;
                font-size: 18px;
                line-height: 27px;
                order: 1;

                @media only screen and (min-width: 768px) {
                font-size: 20px;
                line-height: 30px;
                    order: 0;
                }
            }

            a {
                color: #F56A75;
            }
        }
    }
</style>
