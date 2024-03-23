<template>
  <div>
    <HeaderComponent />
    <BannerComponent />
    <SpotlightComponent />
    <QuickLinksComponent />
    <FooterComponent />
  </div>
</template>


<script>
import HeaderComponent from '../components/HeaderComponent.vue';
import BannerComponent from '../components/BannerComponent.vue';
import SpotlightComponent from '../components/SpotlightComponent.vue'
import QuickLinksComponent from '../components/QuickLinksComponent.vue';
import FooterComponent from '../components/FooterComponent.vue'


export default {
  components: {
    HeaderComponent,
    BannerComponent,
    SpotlightComponent,
    QuickLinksComponent,
    FooterComponent
  },

}
</script>