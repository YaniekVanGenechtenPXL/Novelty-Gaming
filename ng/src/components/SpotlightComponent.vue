<template>
  <div id="spotlightContainer">
    <SpotlightItemComponent v-for="(item, index) in SpotlightItems" :key="index" :item="item" />
  </div>
</template>

<script>
import SpotlightItemComponent from '../components/SpotlightItemComponent.vue'

import mousepad from '../assets/mousepad.png';
import keyboard from '../assets/keyboard.png';

export default {
  components: {
    SpotlightItemComponent
  },
  data() {
    return {
      SpotlightItems: [
        {
          title: 'Authentic mousepads',
          desc: 'Up to 50 different designs',
          img: mousepad,
          buttonTxt: 'Get your pad'
        },
        {
          title: 'Custom keyboards',
          desc: 'Multiple keyboard styles',
          img: keyboard,
          buttonTxt: 'Get your board'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
div#spotlightContainer {
  width: 80vw;
  margin: 100px auto 70px auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 50px;
}

@media (max-width: 1100px) {
  div#spotlightContainer {
    flex-direction: column;
  }
}
</style>