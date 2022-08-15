<template>
  <div class="page">
    <page-header></page-header>
    <page-main v-model:goods="goods"></page-main>
  </div>
</template>

<script>
import shortid from 'shortid';
import pageHeader from './components/Header.vue';
import pageMain from './components/Main.vue';

export default {
  name: 'App',
  components: {
    pageHeader,
    pageMain,
  },

  data() {
    return {
      goods: [
        {
          id: shortid.generate(),
          title: 'params',
          description: 'loreo',
          price(number) {
            return number.toLocaleString('ru-RU');
          },
          scrImg: 'https://i.imgur.com/13x8uMi.jpeg',
        },
        {
          id: shortid.generate(),
          title: 'params',
          description: 'loreo',
          price(number) {
            return number.toLocaleString('ru-RU');
          },
          scrImg: 'https://i.imgur.com/13x8uMi.jpeg',
        },
        {
          id: shortid.generate(),
          title: 'params',
          description: 'loreo',
          price(number) {
            return number.toLocaleString('ru-RU');
          },
          scrImg: 'https://i.imgur.com/13x8uMi.jpeg',
        },
        {
          id: shortid.generate(),
          title: 'params',
          description: 'loreo',
          price(number) {
            return number.toLocaleString('ru-RU');
          },
          scrImg: 'https://i.imgur.com/13x8uMi.jpeg',
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import '@/assets/css/normalize.scss';
@import '@/assets/fonts/fonts.css';
@import '@/assets/css/main.scss';
// @import '@/assets/css/variables.scss';

::-webkit-scrollbar {
  width: 0 !important;
}
// work in Chrome, Yandex, not Mozilla :{

input::-webkit-outer-spin-button,
input::-webkit-inner-spin-button {
  /* display: none; <- Crashes Chrome on hover */
  -webkit-appearance: none;
  margin: 0; /* <-- Apparently some margin are still there even though it's hidden */
}

.page {
  height: 100vh;
  display: grid;
  grid-template-rows: auto 1fr;
  font-family: 'Source Sans Pro';
}
</style>
