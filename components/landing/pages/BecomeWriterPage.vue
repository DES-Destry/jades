<template>
  <div class="main">
    <div class="jasper">JASPER MOCK</div>

    <div class="content">
      <div class="title">Become a writer!</div>
      <div class="description">
        Write helpful articles to help other peoples rich knowledge
      </div>
      <div class="go-button">
        <base-button text="Let's go!" link="/test" hint="I'm ready!" />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import BaseButton from '@/components/BaseButton.vue';

export default Vue.extend({
  name: 'BecomeWriterPage',
  components: { BaseButton },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/colors.scss';

.main {
  height: 100vh;
  width: 100vw;

  background-color: $white;

  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
}

.jasper {
  width: 420px;
  height: 560px;
  margin-left: 121px;
  margin-top: 270px;

  border: 5px solid $primary;
  border-radius: 20px;

  text-align: center;
  color: $gray;
  font-size: 48px;
}

.content {
  margin-right: 121px;
  margin-top: 423px;
}

.title {
  width: 737px;
  height: 100px;

  font-style: normal;
  font-weight: 700;
  font-size: 96px;
  line-height: 112px;
  text-align: right;

  /* spec-green-gradient */

  background: $primary_gradient;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.description {
  font-style: normal;
  font-weight: 250;
  font-size: 28px;
  line-height: 33px;
  display: flex;
  align-items: flex-end;
  justify-content: flex-end;
  text-align: right;

  color: $gray;
}

.go-button {
  display: flex;
  justify-content: flex-end;
  margin-top: 20px;
}
</style>
