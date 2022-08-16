<template>
  <div class="page">
    <header class="page__header">
      <div class="container container_header">
        <div class="header__title">Добавление товара</div>
        <UiDropdown v-model:selected="selected"></UiDropdown>
      </div>
    </header>
    <main class="page__main">
      <div class="container container_main">
        <aside class="main__form aside__form">
          <asideForm @handleSubmit="handleSubmit"></asideForm>
        </aside>
        <pageCards :goods="controlGoods" @handleDelete="handleDelete"></pageCards>
      </div>
    </main>
  </div>
</template>

<script>
import shortid from 'shortid';
import asideForm from './components/UiForm.vue';
import pageCards from './components/Cards.vue';
import UiDropdown from './components/Dropdown.vue';

const directions = {
  asc: 1,
  desc: -1,
  Default: false,
  title_asc: 'text',
};

export default {
  name: 'App',
  components: {
    asideForm,
    pageCards,
    UiDropdown,
  },

  data() {
    return {
      goods: [
        {
          id: shortid.generate(),
          title: 'А',
          description: 'loreo',
          price: 5000,
          scrImg: 'https://i.imgur.com/13x8uMi.jpeg',
        },
        {
          id: shortid.generate(),
          title: 'Б',
          description: 'loreo',
          price: 10000,
          scrImg: 'https://i.imgur.com/13x8uMi.jpeg',
        },
        {
          id: shortid.generate(),
          title: 'Д',
          description: 'loreo',
          price: 90000,
          scrImg: 'https://i.imgur.com/13x8uMi.jpeg',
        },
        {
          id: shortid.generate(),
          title: 'params',
          description: 'loreo',
          price: 10000,
          scrImg: 'https://i.imgur.com/13x8uMi.jpeg',
        },
      ],

      id: null,
      selected: 'Default',
      directions,
    };
  },

  computed: {
    controlGoods() {
      const direction = directions[this.selected];
      return !direction
        ? this.goods
        : [...this.goods].sort((el1, el2) => {
            return direction === 'text'
              ? 1 * el1.title.localeCompare(el2.title, 'ru')
              : direction * (el1.price - el2.price);
          });
    },
  },

  mounted() {
    this.goods = JSON.parse(localStorage.getItem('carts')) || [];
  },

  methods: {
    handleSubmit(data) {
      this.goods.push({ ...data, price: data.price.replace(/\s/g, ''), id: shortid.generate() });
      localStorage.setItem('carts', JSON.stringify(this.goods));
    },

    handleDelete(id) {
      this.goods = this.goods.filter((el) => el.id !== id);
      localStorage.setItem('carts', JSON.stringify(this.goods));
    },
  },
};
</script>

<style lang="scss">
@import '@/assets/css/normalize.scss';
@import '@/assets/fonts/fonts.css';
@import '@/assets/css/main.scss';
@import '@/assets/css/variables.scss';

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

.page__header {
  padding-top: 2rem;
  position: relative;
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
    word-wrap: break-word;

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
