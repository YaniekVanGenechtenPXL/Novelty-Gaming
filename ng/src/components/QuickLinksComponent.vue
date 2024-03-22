<template>
  <div id="container">
    <ul>
      <QuickLinksItemComponent v-for="(item, index) in QuickLinksItems" :key="index" :item="item" />
    </ul>
  </div>
</template>

<script>
import QuickLinksItemComponent from '../components/QuickLinksItemComponent.vue'

export default {
  components: {
    QuickLinksItemComponent
  },
  data() {
    return {
      QuickLinksItems: [
        { img: 'src/assets/icons/order.png', label: 'Order status', url: '/' },
        { img: 'src/assets/icons/gift.png', label: 'Redeem code', url: '/' },
        { img: 'src/assets/icons/smiley.png', label: 'Reviews', url: '/' },
        { img: 'src/assets/icons/contact.png', label: 'Contact us', url: '/' }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
div#container {
  width: 80vw;
  margin: 100px auto;
  display: flex;
  ul {
    width: 100%;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }
}
</style>