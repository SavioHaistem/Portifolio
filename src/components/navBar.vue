<script>
export default {
  props: {
    name: String
  }
}
</script>

<template>
  <nav class="nav-bar">
    <p class="user-name">{{ name }}</p>
  </nav>
</template>

<style>
nav.nav-bar {
  height: fit-content;
  border: 1px solid yellow;
}
p.user-name {
  margin: 3px !important;
  border: 1px solid rgb(255, 0, 238);
  color: white;
  font-family: Legendary;
  font-size: xxx-large;
}
</style>