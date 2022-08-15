<template>
  <form class="form-group">
    <ui-input v-model="formData.title"  label="Наименование товара" placeholder="Введите наименование товара"></ui-input>
    <ui-text-area v-model="formData.description" label="Описание товара" placeholder="Введите описание товара"></ui-text-area>
    <ui-input v-model="formData.scrImg" label="Ссылка на изображение товара" placeholder="Введите ссылку на изображение товара"></ui-input>
    <ui-input v-model="formData.price" label="Цена товара" type="number" placeholder="Введите цену товара"></ui-input>
    <button class="button" disabled="disabled">Добавить товар</button>
  </form>
</template>

<script>
import { klona } from 'klona';
import UiInput from './Input.vue';
import UiTextArea from './uiTextArea.vue';

export default {
  name: 'asideForm',

  components: { UiInput, UiTextArea },

  props: {
    goods: {
      type: Object,
      required: true,
      default()  {
        return {}
      },
    }
  },

  data() {
    return {
      localGoods: klona(this.goods),
      formData: {
        title: null,
        description: null,
        price: null,
        scrImg: null,
      }
    } 
  },

  watch: {
    'formData.price'(newValue, oldValue) {
      console.log(newValue, oldValue);
    }
  }
 
  


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
  /* transition: opacity 200ms ease-in-out, background 200ms ease-in-out; */
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

// /* primary block

//     &_primary
//         background-color: var(--primary-background-color)
//         color: var(--primary-color)

//     &_primary:hover
//         background-color: var(--primary-hover)

// /* secondary block */

// /* .button_secondary {
//  background-color: var(--secondary-background-color);
//  color: var(--secondary-color);

//     &_secondary:hover
//         background-color: var(--secondary-hover)

// /* alternate block */

// /* .button_alternate {
//  background-color: var(--alternate-background-color);
//  color: var(--alternate-color);
//  box-sizing: border-box;
//  border: 1px solid #ACB5BD;

//     &_alternate:hover
//         border: 1px solid #212429
// }  */
</style>
