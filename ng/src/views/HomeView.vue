<template>
  <div>
    <HeaderComponent />
    <BannerComponent />
    <SpotlightComponent />
  </div>
</template>


<script>
import HeaderComponent from '../components/HeaderComponent.vue';
import BannerComponent from '../components/BannerComponent.vue';
import SpotlightComponent from '../components/SpotlightComponent.vue'

export default {
  components: {
    HeaderComponent,
    BannerComponent,
    SpotlightComponent
  },

}
</script>