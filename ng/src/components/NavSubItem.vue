<template>
  <li>
    <router-link :to="item.url" @click="handleClick">
      <img :src="item.icon" :alt="item.label" />
    </router-link>
  </li>
</template>
  
<script>
export default {
  props: {
    item: {
      type: Object,
      required: true
    }
  },
  methods: {
    handleClick() {
      if (this.item.label === 'Main navigation') {
      }
    }
  }
}
</script>
  
  <style lang="scss" scoped>
li {
  list-style: none;
  a {
    top: 0;
    left: 0;
    height: 100%;
    width: 100%;
    display: flex;
    align-items: flex-start;
    gap: 10px;
    img {
      height: 20px;
    }
  }
}

li img[alt='Main navigation'] {
  display: none;
}

@media (max-width: 1100px) {
  li {
    a {
      gap: 0;
      padding: 10px;
    }
  }
  li img[alt='Main navigation'] {
    display: block;
  }
}
</style>