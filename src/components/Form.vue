<template>
  <form class="form-group">
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
        <input
          class="form-group__control"
          type="text"
          id="input_success"
          placeholder="Введите наименование товара"
          value="Success"
        />
      </div>
    </div>
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
          value="Success"
        />
      </div>
    </div>
    <div class="input__control">
      <label for="input_success" class="form-group__label">
        <span class="label__text"> Ссылка на изображение товара </span>
        <div class="form-group__icon">
          <svg width="4" height="4" viewBox="0 0 4 4" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect width="4" height="4" rx="2" fill="#FF8484" />
          </svg>
        </div>
      </label>
      <div class="form-group__input">
        <input
          class="form-group__control"
          type="text"
          id="input_success"
          placeholder="Введите ссылку"
          value="Success"
        />
      </div>
    </div>
    <div class="input__control">
      <label for="input_success" class="form-group__label">
        <span class="label__text"> Цена товара </span>
        <div class="form-group__icon">
          <svg width="4" height="4" viewBox="0 0 4 4" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect width="4" height="4" rx="2" fill="#FF8484" />
          </svg>
        </div>
      </label>
      <div class="form-group__input">
        <input class="form-group__control" type="text" id="input_success" placeholder="Введите цену" value="Success" />
      </div>
    </div>
    <button class="button" disabled="disabled">Добавить товар</button>
  </form>
</template>

<script>
export default {
  name: 'asideForm',
};
</script>

<style lang="scss" scoped>
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
  }

  &__input &__control {
    background: $white;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;

    font-family: 'Inter';
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    line-height: 26px;
    padding-top: 10px;
    padding-left: 16px;
    padding-bottom: 11px;
    width: 100%;
    outline: none;
    border: none;
    box-sizing: border-box;
  }

  &__control_textarea {
    resize: none;
    
    overflow: hidden;
  }
}

// /* .form-group .form-group__input .form-group__control:focus {
//  border: 1px solid var(--blue-3);
//  box-shadow: 0px 1px 1px rgba(51, 154, 240, 0.1);

//     &_success .form-group__input .form-group__control:focus
//         border: 1px solid var(--blue-3)
//         box-shadow: 0px 1px 1px rgba(51, 154, 240, 0.1)

//     &_invalid .form-group__input .form-group__control:focus
//         border: 1px solid var(--red)
//         box-shadow: 0px 1px 1px rgba(240, 61, 62, 0.1)
//         border-radius: 8px
// } */

/* button block */

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
