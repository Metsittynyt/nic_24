<template>
    <TopNav />
    <FlagLine />
    <PageBanner :bannerClass="bannerClass" />
    <FlagLine />
    <div class="page">
      <router-view />
    </div>
    <FlagLine />
    <BottomFooter />
</template>

<script>
import { computed } from 'vue';
import { useRoute } from 'vue-router';
import TopNav from './components/TopNav.vue'
import FlagLine from './components/FlagLine.vue'
import PageBanner from './components/PageBanner.vue'
import BottomFooter from './components/BottomFooter.vue'

export default {
  name: 'App',
  components: {
    TopNav,
    FlagLine,
    PageBanner,
    BottomFooter
  },
  setup() {
    const route = useRoute();
    const bannerClass = computed(() => route.meta.bannerClass || '');

    return { bannerClass };
  }
}
</script>
