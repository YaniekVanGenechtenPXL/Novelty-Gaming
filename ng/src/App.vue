<script setup>
import { RouterView } from 'vue-router'
</script>

<template>
  <RouterView />
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "tt-commons-pro", sans-serif;
  font-style: normal;
}

body {
  background-color: var(--white);
}

:root {
  --black: #231F20;
  --white: #F9F9F9;
}
</style>