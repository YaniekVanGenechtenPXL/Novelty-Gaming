<template>
  <li>
    <router-link :to="item.url">
      <img :src="item.img" :alt="item.label" />
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
  background-color: var(--black);
  width: calc(25% - 15px);
  margin-bottom: 30px;
  a {
    text-decoration: none;
    color: var(--white);
    background-color: var(--black);
    display: flex;
    align-items: center;
    gap: 20px;
    padding: 30px 20px;
    img {
      height: 40px;
    }
    p {
      font-size: 1.2vw;
      font-weight: 300;
    }
  }
}

@media (min-width: 1100px) and (max-width: 1500px) {
  li {
    a {
      p {
        font-size: 1.5vw;
      }
    }
  }
}

@media (min-width: 720px) and (max-width: 1100px) {
  li {
    width: calc(50% - 15px);
    a {
      p {
        font-size: 2vw;
      }
    }
  }
}

@media (max-width: 720px) {
  li {
    width: 100%;
    a {
      padding-left: 40px;
      p {
        font-size: 5vw;
      }
    }
  }
}
</style>