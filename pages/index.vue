<template>
  <div class="main">
    <landing-header />
    <primary-page />
    <become-writer-page />
    <popular-writers />
    <popular-articles />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import LandingHeader from '@/components/landing/LandingHeader.vue';
import PrimaryPage from '@/components/landing/pages/PrimaryPage.vue';
import BecomeWriterPage from '@/components/landing/pages/BecomeWriterPage.vue';
import PopularWriters from '@/components/landing/pages/PopularWriters.vue';
import PopularArticles from '@/components/landing/pages/PopularArticles.vue';

export default Vue.extend({
  name: 'IndexPage',
  components: {
    LandingHeader,
    PrimaryPage,
    BecomeWriterPage,
    PopularWriters,
    PopularArticles,
  },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/colors.scss';

landing-header {
  z-index: 99;
}

primary-page {
  z-index: 10;
}
</style>

<style>
body {
  margin: 0 !important;
}
</style>
