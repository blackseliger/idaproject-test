<template>
  <header class="page__header">
    <div class="container container_header">
      <div class="header__title">Добавление товара</div>
      <UiDropdown></UiDropdown>
    </div>
  </header>
</template>

<script>
import UiDropdown from './Dropdown.vue';

export default {
  name: 'pageHeader',

  components: {
    UiDropdown,
  },
};
</script>

<style lang="scss" scoped>
.page__header {
  padding-top: 2rem;
  position: relative;
}

.container {
  max-width: 1376px;
  margin: 0 auto;
}

.container_header {
  display: flex;
  justify-content: space-between;
}

.header__title {
  font-family: 'Source Sans Pro', sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 35px;
  color: var(--brown);
}
/* Добавление товара */
</style>
