<template>
  <div class="input__control">
    <label for="input_success" class="form-group__label">
      <span class="label__text"> Наименование товара </span>
      <div class="form-group__icon">
        <svg width="4" height="4" viewBox="0 0 4 4" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect width="4" height="4" rx="2" fill="#FF8484" />
        </svg>
      </div>
    </label>
    <div class="form-group__input">
      <input  class="form-group__control" 
      :class="{
        'form-group__control_error': isFill, 
        'form-group__control_success': !isFill, 
        }"  
      type="text" id="input_success" :placeholder="placeholder" v-model="value" />
      <span v-if="isFill" class="form-group__error-message">Поле является обязательным</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UiInput',

  props: {
    label: {
      type: String,
      required: true,
    },
    placeholder: {
      type: String,
      required: true,
    },
  },

  data() {
    return {
      value: null,
    //   isFill: false,
    };
  },

  computed: {
    isFill() {
      return this.value !== '' ? false : true;
    },
  },
};
</script>

<style lang="scss" scoped>

</style>