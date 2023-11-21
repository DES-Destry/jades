<template>
  <div class="all">
    <div :class="`main-button ${isDefaultDark ? 'darker-button' : ''}`">
      <nuxt-link :to="link" class="button-text">{{ text }}</nuxt-link>
    </div>
    <div class="hint">{{ hint }}</div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'BaseButton',
  props: {
    text: {
      type: String,
      required: true,
    },
    hint: {
      type: String,
      default: '',
      required: false,
    },
    icon: {
      type: String,
      default: '',
      required: false,
    },
    link: {
      type: String,
      default: '',
      required: false,
    },
    isDefaultDark: {
      type: Boolean,
      default: false,
      required: false,
    },
  },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/colors.scss';

.all {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.main-button {
  width: 200px;
  height: 50px;

  border: 4px solid $primary;
  background: $primary;
  border-radius: 15px;

  cursor: pointer;

  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

  text-decoration: none;

  z-index: 5;
}

.darker-button {
  background: $secondary !important;
  .button-text {
    color: $primary !important;
  }
}

.main-button:hover {
  background: $primary_gradient !important;
  border: 5px solid $primary_gradient;
  .button-text {
    color: $black !important;
  }
}

.main-button:hover + .hint {
  -webkit-transform: translateY(0px) !important;
  -moz-transform: translateY(0px) !important;
  -o-transform: translateY(0px) !important;
  -ms-transform: translateY(0px) !important;
  transform: translateY(0px) !important;
  color: $primary !important;
}

.main-button:active {
  background: $primary_gradient_revert;
  border: 5px solid $primary_gradient_revert;
}

.button-text {
  text-decoration: none;
  color: $black;

  font-style: normal;
  font-weight: 500;
  font-size: 24px;
  line-height: 28px;
  letter-spacing: 0.01em;

  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hint {
  user-select: none;
  -webkit-touch-callout: none; /* iOS Safari */
  -webkit-user-select: none; /* Chrome/Safari/Opera */
  -khtml-user-select: none; /* Konqueror */
  -moz-user-select: none; /* Firefox */
  -ms-user-select: none; /* Internet Explorer/Edge */

  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 21px;
  letter-spacing: 0.01em;

  color: transparent;

  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  width: 80%;
  transform: translateY(-50px);

  -webkit-transition: 0.3s ease-in-out;
  -moz-transition: 0.3s ease-in-out;
  -o-transition: 0.3s ease-in-out;
  transition: 0.3s ease-in-out;

  z-index: 2;
}
</style>
