<template>
  <div class="mother">
    <mainHome v-if="!isMobile()" />
    <mobileHome v-if="isMobile()" />
  </div>
</template>

<script>
// eslint-disable-next-line
import mainHome from '@/components/HomePage.vue';

// eslint-disable-next-line
import mobileHome from '@/components/MobileHomePage.vue';

export default {
  name: 'Home',
  components: {
    mainHome,
    mobileHome,
  },
  methods: {
    isMobile() {
      if (/Android|webOS|iPhone|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
        return true;
      }
      return false;
    },
  },
};
</script>

<style></style>
