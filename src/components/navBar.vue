<script>
export default {
  props: {
    name: String
  }
}
</script>

<template>
  <header class="main-header">
    <p class="user-name">{{ name }}</p>
  </header>
</template>

<style>
header.main-header {
  height: fit-content;
}
p.user-name {
  margin: 3px !important;
  padding: 2rem 0 0 2rem;
  color: #efefef;
  font-family: Legendary;
  font-size: 60px;
}
</style>