<template>
  <header class="page__header">
    <div class="container container_header">
      <div class="header__title">Добавление товара</div>
      <!-- <div class="header__dropdown" :class="{ dropdown_opened: activeDropdown }">
                     -->
      <div class="header__dropdown" :class="{ dropdown_opened: activeDropdown }">
        <button type="button" class="dropdown__toggle dropdown__toggle_icon" @click="toggleDropdown">
          <!-- <ui-icon icon="tv" class="dropdown__icon" h/> -->
          <span>По умолчанию</span>
        </button>

        <!-- <button
                        type="button"
                        class="dropdown__toggle"
                        :class="{ dropdown__toggle_icon: findIcon }"
                        @click="toggleDropdown"
                      >
                        <ui-icon v-if="actualOption.icon" :icon="actualOption.icon" class="dropdown__icon" />
                        <span>{{ actualOption.text }}</span>
                      </button> -->

        <!-- <div v-show="activeDropdown" class="dropdown__menu" role="listbox">
                        <button v-for="(option, index) in options" :key="`${option.key}-${index}`"
                            class="dropdown__item" :class="{ dropdown__item_icon: findIcon }" role="option"
                            type="button" :value="option.value" @click="select($event.target.value)">
                            <ui-icon v-if="option.icon" :icon="option.icon" class="dropdown__icon" />
                            {{ option.text }}
                        </button>
                    </div> -->
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'pageHeader',
};
</script>

<style lang="scss" scoped>
.page__header {
  padding-top: 2rem;
}

.container {
  max-width: 1376px;
  margin: 0 auto;
}

.container_header {
  display: flex;
  justify-content: space-between;
}

.header__title {
  /* Добавление товара */
  font-family: 'Source Sans Pro', sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 28px;
  line-height: 35px;
  color: var(--brown);
}

.header__dropdown {
  position: relative;
  display: inline-block;

  background: #fffefb;
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 10%);
  border-radius: 4px;

  position: relative;
  display: inline-block;
  background: var(--white);
  box-shadow: 0px 2px 5px rgba(0, 0, 0, 10%);
  border-radius: 4px;
  padding: 10px 27px 11px 16px;
}

.dropdown__toggle {
  display: inline-block;
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 15px;
  color: #b4b4b4;

  background-color: var(--white);
  border: none;
  position: relative;
  text-align: center;
  transition-duration: 0.2s;
  transition-property: background-color, fill, color;
  outline: none;
  box-shadow: none;
  cursor: pointer;
  text-decoration: none;
}

.dropdown__toggle:after {
  content: '';
  position: absolute;
  top: 6px;
  left: calc(100% + 5px);
  transform: none;
  background: url('@/assets/icons/icon-chevron-down.svg') no-repeat;
  background-size: cover;
  display: block;
  width: 8px;
  height: 6px;
  transition: 0.2s transform;
}

/* .dropdown__toggle.dropdown__toggle_icon {
    padding-left: 56px;
} */

.dropdown_opened .dropdown__toggle {
  border-color: var(--blue);
  border-bottom-color: transparent;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}

.dropdown_opened .dropdown__toggle:after {
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
  padding: 8px 16px;
  font-weight: 500;
  font-size: 20px;
  line-height: 28px;
  background-color: var(--white);
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
  background-color: var(--grey-light);
}

.dropdown__item.dropdown__item_icon {
  padding-left: 56px;
  position: relative;
}

.dropdown__item.dropdown__item_icon .dropdown__icon,
.dropdown__toggle_icon .dropdown__icon {
  position: absolute;
  top: 50%;
  left: 16px;
  transform: translate(0, -50%);
}
</style>


