<script >

import AppNav from './components/AppNav.vue';
import AppContent from './components/AppContent.vue';
import AppBody from './components/AppBody.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppNav,
    AppContent,
    AppBody,
    AppFooter,
  }

}

</script>

<template>
  <AppNav></AppNav>
  <AppContent></AppContent>
  <AppBody></AppBody>
  <AppFooter></AppFooter>
</template>

<style lang="scss">
@use '../src/styles/mixins' as *;
@use '../src/styles/variables' as *;
</style>
