<template>
  <li>
    <router-link :to="item.url">
      <img :src="item.icon" :alt="item.label" />
      <p>{{ item.label }}</p>
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
    align-items: center;
    gap: 10px;
    text-decoration: none;
    color: black;
    font-size: 18px;
    img {
      height: 20px;
    }
  }
}
</style>