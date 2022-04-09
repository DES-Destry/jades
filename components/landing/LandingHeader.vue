<template>
  <div class="header-main">
    <header>
      <div class="links">
        <landing-header-button
          v-for="link in links"
          :key="link"
          :name="link.name"
          :url="link.url"
        ></landing-header-button>
      </div>
    </header>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import LandingHeaderButton from './LandingHeaderButton.vue';

type LandingHeaderData = {
  links: {
    name: string;
    url: string;
  }[];
};

export default Vue.extend({
  name: 'LandingHeader',
  components: { LandingHeaderButton },
  data: (): LandingHeaderData => {
    return {
      links: [
        {
          name: 'Articles',
          url: '/articles',
        },
        {
          name: 'Writers',
          url: '/users',
        },
        {
          name: 'Marketplace',
          url: '/marketplace',
        },
        {
          name: 'Bids',
          url: '/bids',
        },
        {
          name: 'Traders',
          url: '/traders',
        },
      ],
    };
  },
});
</script>

<style lang="scss" scoped>
@import '@/assets/styles/colors.scss';

.header-main {
  /* Header position */
  width: 100vw;
  height: 121px;
  position: fixed;
  left: 0%;
  right: 0%;
  top: 0%;
  bottom: 0%;

  /* Header glass effect */
  background: $glass;
  border: 1px solid $secondary;
  box-sizing: border-box;
  backdrop-filter: blur(40px);

  z-index: 9999;
}

.links {
  height: 100%;
  display: flex;
  justify-content: flex-start;
  margin-left: 121px;
  margin-top: 41px;
}
</style>
