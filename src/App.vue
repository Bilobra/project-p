<template>
  <div id="app">
    <div class=" d-flex flex-column p-0">
      <HeaderComponent />
      <MainSection/>
      <FooterSection />
    </div>
  </div>
</template>

<script>

import HeaderComponent from './HeaderComponent.vue';
import FooterSection from './FooterSection.vue';
import MainSection from './MainSection.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    FooterSection,
    MainSection,
  }
}
</script>

<style lang="scss">

</style>
