<template>
  <div class="main">
    <div class="content">
      <div class="title">Most popular writers</div>
      <div class="writers">
        <!-- <writer-slide /> -->
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
// import WriterSlide from '@/components/landing/WriterSlide.vue';

export default Vue.extend({
  name: 'PopularWriters',
  // components: { WriterSlide },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/colors.scss';

.main {
  height: 100vh;
  width: 100vw;

  background-color: $secondary;
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

.writers {
  width: calc(100% - 121px);
  height: 548px;
  margin-top: 50px;

  background: linear-gradient(
    134.4deg,
    rgba(255, 255, 255, 0.4) 12.35%,
    rgba(255, 255, 255, 0.1) 72.5%
  );
  box-shadow: 0px 4px 24px -1px rgba(0, 0, 0, 0.2);
  backdrop-filter: blur(40px);

  border-radius: 40px;
  border: 2px solid $primary;
}
</style>
