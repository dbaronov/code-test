<script setup lang="ts">
  import Header from './components/Header.vue'
  import PromoImage from './components/PromoImage.vue'
  import PromoBanner from './components/PromoBanner.vue'
  import CardDeck from './components/CardDeck.vue'
  import Quote from './components/Quote.vue'
  import Form from './components/Form.vue'
  import Footer from './components/Footer.vue'
</script>

<template>
  <div>
    <Header msg="Logo + Menu" />

    <section class="content-copy">
      <h1>We Do Awesome Things</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    </section>

    <section class="promo">
      <PromoImage imgUrl="./assets/images/brand/browser-image.png" />
      <PromoBanner />
    </section>

    <section class="content-copy">
      <h2>We Do Really Awesome Things</h2>
      <p>Lorem ipsum dolor sit amet, link consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    </section>

    <section class="deck">
      <Suspense>
        <CardDeck imgUrl="./assets/images/brand/icon/service-badge.png" />
      </Suspense>
    </section>

    <section class="quote">
      <Quote />
    </section>

    <section class="content-copy">
      <h2>Contact About Awesomeness</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
    </section>

    <section class="form">
      <Form />
    </section>

    <section class="footer">
      <Footer imgUrl="./assets/images/brand/icon/service-badge.png" />
    </section>

  </div>
</template>

<style lang="scss">
  #app {
    position: relative;
    font-family: Helvetica, Arial, sans-serif;

    .roboto-thin {
      font-family: "Roboto", sans-serif;
      font-weight: 100;
      font-style: normal;
    }

    .roboto-light {
      font-family: "Roboto", sans-serif;
      font-weight: 300;
      font-style: normal;
    }

    .roboto-regular {
      font-family: "Roboto", sans-serif;
      font-weight: 400;
      font-style: normal;
    }

    .roboto-medium {
      font-family: "Roboto", sans-serif;
      font-weight: 500;
      font-style: normal;
    }

    .roboto-bold {
      font-family: "Roboto", sans-serif;
      font-weight: 700;
      font-style: normal;
    }

    .roboto-black {
      font-family: "Roboto", sans-serif;
      font-weight: 900;
      font-style: normal;
    }

    .roboto-thin-italic {
      font-family: "Roboto", sans-serif;
      font-weight: 100;
      font-style: italic;
    }

    .roboto-light-italic {
      font-family: "Roboto", sans-serif;
      font-weight: 300;
      font-style: italic;
    }

    .roboto-regular-italic {
      font-family: "Roboto", sans-serif;
      font-weight: 400;
      font-style: italic;
    }

    .roboto-medium-italic {
      font-family: "Roboto", sans-serif;
      font-weight: 500;
      font-style: italic;
    }

    .roboto-bold-italic {
      font-family: "Roboto", sans-serif;
      font-weight: 700;
      font-style: italic;
    }

    .roboto-black-italic {
      font-family: "Roboto", sans-serif;
      font-weight: 900;
      font-style: italic;
    }

  }

  .content-copy {
    margin: 20px auto;
    padding: 20px 15px;
    text-align: center;
    font-weight: 400;

    @media only screen and (min-width: 768px) {
      max-width: 730px;
      margin: 60px auto;
    }

    h1, h2 {
      font-size: 32px;
      line-height: 40px;
      color: #0E3757;
      margin-bottom: 10px;

      @media only screen and (min-width: 768px) {
        font-size: 50px;
        line-height: 64px;
      }
    }

    p {
      font-size: 20px;
      line-height: 30px;
      color: #8D9CA8;

      @media only screen and (min-width: 768px) {
        font-size: 24px;
        line-height: 36px;
      }
    }
    
  }
</style>
