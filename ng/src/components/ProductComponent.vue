<template>
  <div id="itemContainer">
    <div>
      <img :src="getImagePath" :alt="product.title" />
      <h2>{{ product.title }}</h2>
      <p>€{{ product.price }}</p>
    </div>
  </div>
</template>
  
<script>
import { defineComponent } from 'vue'
import Black_MP from '../assets/products/Black_MP.jpg'
import BlackV2_MP from '../assets/products/BlackV2_MP.jpg'
import Pink_MP from '../assets/products/Pink_MP.jpg'
import White_MP from '../assets/products/White_MP.jpg'
import Zebra_MP from '../assets/products/Zebra_MP.jpg'

export default defineComponent({
  props: {
    product: {
      type: Object,
      required: true
    }
  },
  computed: {
    getImagePath() {
      switch (this.product.id) {
        case 1:
          return Black_MP
        case 2:
          return BlackV2_MP
        case 3:
          return Pink_MP
        case 4:
          return White_MP
        case 5:
          return Zebra_MP
        default:
          return ''
      }
    }
  }
})
</script>


<style lang="scss" scoped>
div#itemContainer {
    background-color: var(--white);
    box-shadow: 0px 3px 6px rgba($color: #000000, $alpha: 0.16);
    width: calc(33.333% - 20px);
    div {
        display: flex;
        flex-direction: column;
        padding: 5px;
        img {
            width: 100%;
        }
    }
}

@media (min-width: 1100px) and (max-width: 1600px) {
  div#itemContainer {
    width: calc(50% - 15px);
  }
}

@media (max-width: 1100px) {
  div#itemContainer {
    width: calc(100%);
  }
}
</style>
  