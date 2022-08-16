<template>
  <div class="header__dropdown" :class="{ dropdown_opened: activeDropdown }">
    <template v-if="actualOption === null">
      <button type="button" class="dropdown__toggle" @click="toggleDropdown">
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
    </template>
    <template v-else>
      <button type="button" class="dropdown__toggle" @click="toggleDropdown">
        <span>{{ actualOption.text }}</span>
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
    </template>
    <div v-if="activeDropdown" class="dropdown__menu" role="listbox">
      <button
        v-for="(option, index) in dropdownTypes"
        :key="`${option.key}-${index}`"
        class="dropdown__item"
        role="option"
        type="button"
        :value="option.value"
        @click="selected($event.target.value)"
      >
        {{ option.text }}
      </button>
    </div>
  </div>
</template>

<script>
const dropdownTypes = [
  {
    value: 'Default',
    text: 'По умолчанию',
  },
  {
    value: 'asc',
    text: 'Минимум',
  },
  {
    value: 'desc',
    text: 'Максимум',
  },
  {
    value: 'title_asc',
    text: 'По наименованию ',
  },
];

export default {
  name: 'UiDropdown.vue',
  data() {
    return {
      dropdownTypes,
      selectedType: 'Default',
      activeDropdown: false,
    };
  },

  emits: ['update:selected'],

  methods: {
    toggleDropdown() {
      return this.activeDropdown === false ? (this.activeDropdown = true) : (this.activeDropdown = false);
    },

    selected(value) {
      this.activeDropdown = false;
      this.selectedType = value;
    },
  },

  watch: {
    selectedType: {
      handler() {
        this.$emit('update:selected', this.selectedType);
      }
    }
  },

  computed: {
    actualOption() {
      return this.dropdownTypes.find((option) => {
        if (option.value === this.selectedType) return option;
      });
    },
  },
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
  z-index: 9999;
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
  cursor: $customPointer;
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

.dropdown__icon {
  transition: 0.2s transform ease-in;
}

.dropdown_opened .dropdown__toggle .dropdown__wrapper-icon .dropdown__icon {
  transform: rotate(180deg);
}

.dropdown__menu {
  margin: 0;
  width: 100%;
  padding: 0;
  border-radius: 0 0 8px 8px;
  left: 0;
  background-clip: padding-box;
  display: none;
  flex-direction: column;
  border-top: none;
  overflow: hidden;
  animation: ani 0.5s forwards;
}

@keyframes ani {
  0% {
    transform: translateY(-50%);
  }
  100% {
    transform: translateY(30%);
  }
}

.dropdown_opened .dropdown__menu {
  display: flex;
  position: absolute;
  // transform: translateY(30%);
  top: -1px;
}

.dropdown__item {
  font-family: 'Source Sans Pro';
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 15px;
  padding: 8px 16px;
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
