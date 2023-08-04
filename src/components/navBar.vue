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
}
p.user-name {
  width: fit-content;
  margin: 3px !important;
  padding: 1rem 0 0 1rem;
  color: #00CCCC;
  font-family: Legendary;
  font-size: xxx-large;
}
</style>