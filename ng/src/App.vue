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
  font-family: 'tt-commons-pro', sans-serif;
  font-style: normal;
}

html {
  overflow-x: hidden;
}

body {
  background-color: var(--white);
}

:root {
  --black: #231f20;
  --white: #f9f9f9;
}
</style>