<template>
  <div id="app">
    <div class=" d-flex flex-column p-0">
      <HeaderComponent />
      <MainSection/>
      <!-- <CarouselComponent/> -->
      <FooterSection />

    </div>
  </div>
</template>

<script>

import HeaderComponent from './HeaderComponent.vue';
import FooterSection from './FooterSection.vue';
import MainSection from './MainSection.vue';
// import CarouselComponent from './components/main/CarouselComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    FooterSection,
    MainSection,
    // CarouselComponent
  }
}
</script>

<style lang="scss">
@import './style/General.scss';
</style>
