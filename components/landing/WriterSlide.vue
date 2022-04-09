<template>
  <div class="main"></div>
</template>

<script lang="ts">
import Vue from 'vue';
// import BaseButton from '@/components/BaseButton.vue';

export default Vue.extend({
  name: 'WriterSlide',
  // components: { BaseButton },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/colors.scss';

.main {
  width: 480px;
  height: 192px;
  background: #011e26;
  border-radius: 10px;
}
</style>
