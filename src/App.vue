<script>
import AppHeader from './components/AppHeader.vue';
import AppHeaderNav from './components/AppHeaderNav.vue';
import AppJumbo from './components/AppJumbo.vue';

export default {
  components: {                                 
    AppHeader,
    AppHeaderNav,
    AppJumbo
  },
  data() {
    return {
    }
  }
}

</script>

<template>
  <AppHeader />
  <AppHeaderNav />
  <AppJumbo />
</template>

<style lang="scss">
@use "./style/style.scss" as *;

</style>