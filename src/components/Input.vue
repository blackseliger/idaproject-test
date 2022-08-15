<template>
  <div class="input__control">
    <label for="input_success" class="form-group__label">
      <span class="label__text"> {{ label }} </span>
      <div class="form-group__icon">
        <svg width="4" height="4" viewBox="0 0 4 4" fill="none" xmlns="http://www.w3.org/2000/svg">
          <rect width="4" height="4" rx="2" fill="#FF8484" />
        </svg>
      </div>
    </label>
    <div class="form-group__input">
      <input
        ref="input"
        class="form-group__control"
        :class="{
          'form-group__control_error': isFill,
          'form-group__control_success': !isFill,
        }"
        type="text"
        :placeholder="placeholder"
        :value="modelValue"
        @input="controlInput($event.target.value)"
      />
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
      if (this.type === 'number' && value !== '') {
        if (value.match(/[a-z]/g)) {
          this.$refs['input'].value = '';
          this.$emit('update:modelValue', '');
        } else {
          this.$emit('update:modelValue', new Intl.NumberFormat('ru-RU').format(value.replace(/\s/g, '')));
        }
      } else {
        this.$emit('update:modelValue', value);
      }
    },
  },

  computed: {
    isFill() {
      return this.modelValue !== '' ? false : true;
    },
  },
};
</script>

<style lang="scss" scoped>
</style>