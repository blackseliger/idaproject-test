<template>
  <main class="page__main">
    <div class="container container_main">
      <aside class="main__form aside__form">
        <asideForm goods="goods"></asideForm>
      </aside>
      <pageCards goods="goods"></pageCards>
    </div>
  </main>
</template>

<script>
import asideForm from './UiForm.vue';
import pageCards from './Cards.vue';

export default {
  name: 'PageMain.vue',
  components: { asideForm, pageCards },

  props: {
    goods: {
      type: Object,
      required: true,
      default() {
        return {};
      },
    },
  },
};
</script>

<style lang="scss">
@import '@/assets/css/variables.scss';

.page__main {
  padding-top: 1rem;
}

.container_main {
  display: grid;
  grid-template-columns: 332px 1fr;
  gap: 1rem;
}

.container {
  max-width: 1376px;
  margin: 0 auto;
}

.main {
  &__form {
    padding: 1.5rem;
    background: $white;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
    height: 440px;
    box-sizing: border-box;
    position: sticky;
    top: 24px;
  }
  &__cards {
    display: grid;
    grid-template-columns: repeat(3, 332px);
    gap: 16px;
  }

  &__card {
    display: grid;
    grid-template-columns: 1fr;
    position: relative;
    gap: 16px;
    height: 423px;
  }
}

.card {
  cursor: $customPointer;

  &__icon_delete {
    display: inline-block;
    opacity: 0;
    width: 16px;
    height: 16px;
    top: -8px;
    right: -9.5px;
    padding: 8px 9.5px;
    position: absolute;

    background: #ff8484;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    cursor: $customPointer;
    transition: 0.2s opacity;
  }
  &__wrapper-img {
    width: 100%;
    height: 200px;
    border-radius: 4px 4px 0px 0px;
  }

  &__img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  &__content {
    display: grid;
    grid-template-columns: 1fr;
    padding-left: 1rem;
    padding-right: 1rem;
    padding-bottom: 1.5rem;
    word-break: break-all;
  }

  &__header {
    font-family: 'Source Sans Pro';
    font-style: normal;
    font-weight: 600;
    font-size: 20px;
    line-height: 25px;
    text-align: start;
    color: $brown;
  }

  &__info {
    font-family: 'Source Sans Pro';
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 20px;

    color: $brown;
  }

  &__price {
    font-family: 'Source Sans Pro';
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 30px;

    color: $brown;
  }
}

.card:hover .card__icon_delete {
  opacity: 1;
}

.card:hover {
  box-shadow: 0px 5px 10px 2px rgba(34, 60, 80, 0.2);
}
</style>
