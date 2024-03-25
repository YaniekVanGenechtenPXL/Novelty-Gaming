<template>
  <div id="container">
    <ul>
      <QuickLinksItemComponent v-for="(item, index) in QuickLinksItems" :key="index" :item="item" />
    </ul>
  </div>
</template>

<script>
import QuickLinksItemComponent from '../components/QuickLinksItemComponent.vue'

import orderIcon from '../assets/icons/order.png';
import giftIcon from '../assets/icons/gift.png';
import smileyIcon from '../assets/icons/smiley.png';
import contactIcon from '../assets/icons/contact.png'

export default {
  components: {
    QuickLinksItemComponent
  },
  data() {
    return {
      QuickLinksItems: [
        { img: orderIcon, label: 'Order status', url: '/' },
        { img: giftIcon, label: 'Redeem code', url: '/' },
        { img: smileyIcon, label: 'Reviews', url: '/' },
        { img: contactIcon, label: 'Contact us', url: '/' }
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