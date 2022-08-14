<template>
  <div class="page">
    <page-header></page-header>
    <page-main></page-main>
  </div>
</template>

<script>
import pageHeader from './components/Header.vue';
import pageMain from './components/Main.vue';

export default {
  name: 'App',
  components: {
    pageHeader,
    pageMain,
  },
};
</script>

<style lang="scss">
@import '@/assets/css/normalize.scss';
@import '@/assets/fonts/fonts.css';
@import '@/assets/css/main.scss';


body {
  overflow: hidden;
}

#app {
}

.page {
  height: 100vh;
  display: grid;
  grid-template-rows: auto 1fr;
  font-family: 'Source Sans Pro';
}
</style>
