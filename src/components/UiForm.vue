<template>
  <form class="form-group" @submit.prevent="$emit('handleSubmit', formData)">
    <ui-input v-model="formData.title" label="Наименование товара" placeholder="Введите наименование товара"></ui-input>
    <ui-text-area
      v-model="formData.description"
      label="Описание товара"
      placeholder="Введите описание товара"
    ></ui-text-area>
    <ui-input
      v-model="formData.scrImg"
      label="Ссылка на изображение товара"
      placeholder="Введите ссылку на изображение товара"
    ></ui-input>
    <ui-input v-model="formData.price" label="Цена товара" type="number" placeholder="Введите цену товара"></ui-input>
    <button class="button" :disabled="buttonWork">Добавить товар</button>
  </form>
</template>

<script>
import UiInput from './UiInput.vue';
import UiTextArea from './UiInputText.vue';
// import uiTextArea from './uiTextarea.vue';
const validKeys = ['title', 'price', 'scrImg'];

export default {
  name: 'UiForm.vue',

  components: { UiInput, UiTextArea },

  props: {
    goods: {
      type: Object,
      required: true,
      default() {
        return {};
      },
    },
  },

  emits: ['handleSubmit'],

  data() {
    return {
      formData: {
        title: null,
        description: null,
        price: null,
        scrImg: null,
      },
    };
  },

  computed: {
    buttonWork() {
      let result = true;
      for (const key of validKeys) {
        if (!this.formData[key]) {
          return (result = true);
        } else {
          result = false;
        }
      }
      return result;
    },
  },
};
</script>

<style lang="scss">
@import '@/assets/css/variables.scss';

.form-group {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1rem;

  &__label {
    font-style: normal;
    font-weight: 400;
    font-size: 10px;
    line-height: 13px;
    letter-spacing: -0.02em;

    color: $darkfiol;
    position: relative;
  }

  &__icon {
    display: inline;
    width: 4px;
    height: 4px;
    position: absolute;
  }

  &__input {
    display: inline-flex;
    width: 100%;
    flex-direction: column;
    gap: 4px;
  }

  &__error-message {
    font-family: 'Source Sans Pro';
    font-style: normal;
    font-weight: 400;
    font-size: 8px;
    line-height: 10px;
    letter-spacing: -0.02em;

    color: $ligthRed;
  }

  &__control_error {
    border: 1px solid $ligthRed;
  }

  &__control_success {
    border: none;
  }

  &__control:focus {
    transform: scale(105%);
  }

  &__control {
    background: $white;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;

    font-family: 'Inter';
    font-style: normal;
    font-weight: 400;
    font-size: 12px;
    line-height: 15px;
    text-align: left;
    padding-top: 10px;
    padding-left: 16px;
    padding-bottom: 11px;
    width: 100%;
    outline: none;
    transition: 0.2s transform;
    box-sizing: border-box;
  }

  &__control_textarea {
    resize: none;
    height: 108px;
    overflow: hidden;
    border: none;
  }
}

.button {
  height: 36px;
  border-radius: 10px;
  font-family: 'Inter';
  font-style: normal;
  font-weight: 600;
  font-size: 12px;
  line-height: 15px;
  text-align: center;
  transition: background 200ms ease-in-out;
  padding: 10px 95px 11px 95px;
  border: none;
  cursor: pointer;
  display: inline-block;
  white-space: nowrap;
  background: $lightGreen;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
  border-radius: 10px;

  &:disabled {
    color: #b4b4b4;
    background: $white-disable;
    pointer-events: none;
    box-shadow: none;
  }
}
</style>
