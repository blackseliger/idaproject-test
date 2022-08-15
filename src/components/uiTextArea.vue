<template>
  <div class="input__control">
    <label for="input_success" class="form-group__label">
      <span class="label__text"> Описание товара </span>
    </label>
    <div class="form-group__input">
      <textarea
        class="form-group__control form-group__control_textarea"
        type="text"
        :placeholder="placeholder"
        :value="modelValue"
        @input="controlInput($event.target.value)"
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
    },
    placeholder: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      default: 'text',
    },
    modelValue: {
      type: [String, Boolean, Number, Function],
      required: true,
      default: true,
    },
  },

  data() {},

  methods: {
    controlInput(value) {
      this.$emit('update:modelValue', value);
    },
  },
};
</script>

<style lang="scss">
</style>