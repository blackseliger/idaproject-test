<template>
  <div class="header__dropdown ">
    <button type="button" class="dropdown__toggle">
      <span>По умолчанию</span>
      <div class="dropdown__wrapper-icon">
        <svg
          class="dropdown__icon"
          width="8"
          height="6"
          viewBox="0 0 8 6"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M7.48532 1.24264L4.24268 4.48528L1.00003 1.24264" stroke="#B4B4B4" />
        </svg>
      </div>
    </button>
    <!-- 
    <button type="button" class="dropdown__toggle">
      <span>{{ 'test' }}</span>
      <div class="dropdown__wrapper-icon">
        <svg
          class="dropdown__icon"
          width="8"
          height="6"
          viewBox="0 0 8 6"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path d="M7.48532 1.24264L4.24268 4.48528L1.00003 1.24264" stroke="#B4B4B4" />
        </svg>
      </div>
    </button> -->

    <div class="dropdown__menu" role="listbox">
      <button class="dropdown__item" role="option" type="button">
        {{ 'test2' }}
      </button>
      <button class="dropdown__item" role="option" type="button">
        {{ 'test2' }}
      </button>
      <button class="dropdown__item" role="option" type="button">
        {{ 'test2' }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UiDropdown.vue',
};



</script>

<style lang="scss" scoped>
@import '@/assets/css/variables.scss';

.header__dropdown {
  background: $white;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  width: 121px;
  height: 36px;
  text-align: center;
  padding-top: 10px;
  padding-bottom: 11px;
  box-sizing: border-box;
  position: relative;
  transition: 0.2s transform;
  /* white-space: nowrap; */
  /* padding: 10px 27px 11px 16px; */
}

.dropdown__toggle {
  display: inline-flex;
  gap: 5px;
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 15px;
  color: #b4b4b4;

  background-color: $white;
  border: none;
  transition-duration: 0.2s;
  transition-property: background-color, fill, color, transform;
  outline: none;
  box-shadow: none;
  cursor: pointer;
  text-decoration: none;
}

.header__dropdown:hover {
  transform: scale(110%);
}

.dropdown__wrapper-icon {
  position: absolute;
  width: 8px;
  height: 6px;
  transform: none;
  display: inline-block;
  transition: 0.5s transform;
  left: calc(100% - 16px);
  bottom: calc(100% - 18px);
}

/*.dropdown_opened .dropdown__toggle {
  border-color: var(--blue);
  border-bottom-color: transparent;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
} */

.dropdown_opened .dropdown__toggle .dropdown__wrapper-icon .dropdown__icon {
  transform: rotate(180deg);
}

.dropdown__menu {
  margin: 0;
  width: 100%;
  padding: 0;
  border-radius: 0 0 8px 8px;
  left: 0;
  z-index: 95;
  background-clip: padding-box;
  display: none;
  flex-direction: column;
  border: 2px solid var(--blue);
  border-top: none;
  overflow: hidden;
  transition: 0.5s all;
}

.dropdown_opened .dropdown__menu {
  display: flex;
  position: absolute;
  transform: translate3d(0px, 52px, 0px);
  top: -1px;
  left: 0;
  will-change: transform;
  right: auto;
  bottom: auto;
}

.dropdown__item {
  font-family: 'Source Sans Pro';
  padding: 8px 16px;
  font-weight: 500;
  font-size: 20px;
  line-height: 28px;
  background-color: $white;
  box-shadow: none;
  border: none;
  cursor: pointer;
  text-align: left;
  transition-duration: 0.2s;
  transition-property: background-color, border-color, color;
  outline: none;
  text-decoration: none;
}

.dropdown__item:hover,
.dropdown__item:focus {
  background-color: rgba(119, 218, 143, 0.623);
}
</style>
