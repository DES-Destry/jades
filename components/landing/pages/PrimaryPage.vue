<template>
  <div class="main">
    <div class="content">
      <img class="logo" :src="require('@/assets/images/colored-logo.svg')" />
      <div class="title">JADES</div>
      <div class="description">
        New ultimate place for programmers and designers. Blogging, chatting and
        NFT trading
      </div>
      <div class="buttons">
        <base-button
          class="button"
          text="Sign up"
          link="/sign-up"
          hint="Are you new?"
        />
        <base-button
          class="button"
          text="Sign in"
          link="/sign-in"
          hint="Already have an account?"
          is-default-dark="true"
        />
      </div>
    </div>

    <div class="jasper">JASPER MOCK</div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import BaseButton from '@/components/BaseButton.vue';

export default Vue.extend({
  name: 'PrimaryPage',
  components: { BaseButton },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/colors.scss';

.main {
  height: 100vh;
  width: 100vw;

  background-color: $secondary;

  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
}

.logo {
  width: 124px;
  height: 124px;

  margin-top: 257px;
}

.content {
  margin-left: 121px;
}

.title {
  font-style: normal;
  font-weight: 700;
  font-size: 96px;
  line-height: 112px;

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
  align-items: center;

  color: $white;
}

.jasper {
  width: 480px;
  height: 740px;
  margin-right: 121px;
  margin-top: 199px;

  border: 5px solid $primary;
  border-radius: 20px;

  text-align: center;
  color: $white;
  font-size: 48px;
}

.buttons {
  margin-top: 20px;
  width: 100%;
  height: 100%;

  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: flex-start;
}

.button {
  margin-right: 26px;
}
</style>
