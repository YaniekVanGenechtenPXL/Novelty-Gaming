<template>
  <div>
    <HeaderComponent />
    <BannerComponent />
    <SpotlightComponent />
    <ShopComponent />
    <QuickLinksComponent />
    <FooterComponent />
  </div>
</template>


<script>
import HeaderComponent from '../components/HeaderComponent.vue'
import BannerComponent from '../components/BannerComponent.vue'
import SpotlightComponent from '../components/SpotlightComponent.vue'
import QuickLinksComponent from '../components/QuickLinksComponent.vue'
import FooterComponent from '../components/FooterComponent.vue'
import ShopComponent from '../components/ShopComponent.vue'
 
export default {
  components: {
    HeaderComponent,
    BannerComponent,
    SpotlightComponent,
    ShopComponent,
    QuickLinksComponent,
    FooterComponent
  }
}
</script>