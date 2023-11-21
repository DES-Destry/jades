<template>
  <div class="main">
    <div class="content">
      <div class="title">Most popular articles</div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/colors.scss';

.main {
  height: 100vh;
  width: 100vw;

  background-color: $white;
}

.content {
  margin-left: 121px;
}

.title {
  width: 737px;
  height: 76px;
  padding-top: 189px;

  font-style: normal;
  font-weight: 700;
  font-size: 64px;
  line-height: 75px;

  /* spec-green-gradient */

  background: $primary_gradient;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
</style>
