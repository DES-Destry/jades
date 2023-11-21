<template>
  <div class="button-main">
    <nuxt-link :to="url" class="tab">
      {{ name }}
    </nuxt-link>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'LandingHeaderButton',
  props: {
    name: {
      type: String,
      required: true,
    },
    url: {
      type: String,
      required: true,
    },
  },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/colors.scss';

.tab {
  margin-right: 20px;
  text-decoration: none;

  font-weight: 500;
  font-size: 22px;
  line-height: 26px;

  color: $white;
  background-color: transparent;
  padding: 11px 15px 11px 15px;
  border-radius: 20px;

  animation-duration: 0.5s;
}

.tab:hover {
  animation-name: link-hover;
  animation-timing-function: ease;
  animation-fill-mode: forwards;
}

@keyframes link-hover {
  0% {
    color: $white;
    background-color: transparent;
  }
  100% {
    color: $black;
    background-color: $white;
  }
}
</style>
