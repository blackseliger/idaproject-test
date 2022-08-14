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


<style lang="scss" scoped>
@import '@/assets/css/normalize.css';
@import '@/assets/fonts/fonts.css';
@import '@/assets/css/main.css';

// #app {
//   font-family: Avenir, Helvetica, Arial, sans-serif;
//   -webkit-font-smoothing: antialiased;
//   -moz-osx-font-smoothing: grayscale;
//   // text-align: center;
//   // color: #2c3e50;
//   // margin-top: 60px;
//   overflow: hidden;
// }

.page {
  /* width: 100vw;
    width: 100vh; */
  display: grid;
  grid-template-rows: auto 1fr;
  font-family: 'Source Sans Pro';
  overflow-x: hidden;
}
</style>

