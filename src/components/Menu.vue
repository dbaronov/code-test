<script setup lang="ts">
    import { ref } from 'vue'

    const showModal = ref(false)

</script>

<template>
    <section id="menu">
        <button type="button" aria-label="Expand or collapse main menu" :aria-expanded="showModal" @click="showModal = !showModal"></button>
        
        <nav :aria-hidden="!showModal">
            <ul>
                <li>
                    <a href="#">About Us</a>
                </li>
                <li>
                    <a href="#">About You</a>
                </li>
                <li>
                    <a href="#">Portfolio</a>
                </li>
                <li>
                    <a href="#">Contact</a>
                </li>
            </ul>
        </nav>

    </section>
</template>

<style lang="scss" scoped>
  #menu {
    position: relative;

    @media only screen and (min-width: 768px) {
        background-color: transparent;
    }

    button {
        display: block;
        background-color: transparent;
        border: none;
        width: 32px;
        height: 32px;
        background-image: url(../assets/images/brand/menu/burger.png);

        &[aria-expanded="true"] {
            position: absolute;
            right: 245px;
            top: -16px;
            background-image: url(../assets/images/brand/menu/close.png);
        }
        @media only screen and (min-width: 768px) {
            display: none;
        }
    }

    nav {
        position: fixed;
        top: 0;
        padding: 10px;
        left: 100%;
        bottom: 0;
        background-color: #0E3757;
        z-index: 10;

        &[aria-hidden="false"] {
            left: auto;
            right: 0;
            width: 258px;

            @media only screen and (min-width: 768px) {
                width: auto;
            }
        }

        @media only screen and (min-width: 768px) {
            display: block;
            background-color: transparent;
            position: static;
        }

        ul {
            display: flex;
            flex-direction: column;
            text-align: center;

            @media only screen and (min-width: 768px) {
                text-align: left;
                flex-direction: row;
            }
                li {
                    padding: 10px 5px;
                    margin: 0 5px;

                    &:last-of-type {

                        a {
                            background-color: #F56A75;
                            color: #FFFFFF;
                            padding: 16px 71px;
                            font-size: 16px;
                            border-radius: 4px;

                            @media only screen and (min-width: 768px) { 
                                padding: 16px 32px;
                            }
                        }
                    }

                    a {
                        font-size: 18px;
                        line-height: 30px;
                        padding: 4px 12px;
                        color: #FFFFFF;

                        @media only screen and (min-width: 768px) {
                            color: #0E3757;
                        }
                    }
                }
        }
    }
  }
</style>
