<script >

import AppNav from './components/AppNav.vue';
import AppComics from './components/AppComics.vue';
import AppBody from './components/AppBody.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppNav,
    AppComics,
    AppBody,
    AppFooter,
  }

}

</script>

<template>
  <AppNav></AppNav>
  <AppComics></AppComics>
  <AppBody></AppBody>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use '../src/styles/general.scss' as *;
</style>
