<template>
  <div class="input__control">
    <label for="input_success" class="form-group__label">
      <span class="label__text"> Описание товара </span>
    </label>
    <div class="form-group__input">
      <textarea
        class="form-group__control form-group__control_textarea"
        type="text"
        id="input_success"
        placeholder="Введите описание товара"
        value=""
      />
    </div>
  </div>
</template>

<script>
export default {
  name: 'UiTextArea',

  props: {
    label: {
      type: String,
      required: true,
      default: 'Наименование строки нет',
    },

     placeholder: {
      type: String,
      required: true,
    },
  },
};
</script>

<style lang="scss">
</style>