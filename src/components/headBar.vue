<script>
export default {
  name: "headBar",
  props: {
    name: String
  }
}
</script>

<template>
  <header class="main-header">
    <p class="rune">a</p>
    <p class="user-name">{{ name }}</p>
    <p class="rune">b</p>
  </header>
</template>

<style>
p.rune {
  padding: 0 1rem;
  font-size: 30px;
  color: #7cffca;
  font-family: runes;
}
header.main-header {
  margin-top: 1rem;
  height: 5rem;
  display: flex;
  justify-content: center;
}
p.user-name {
  height: fit-content;
  text-shadow: 1px 2px 70px rgb(0, 188, 209);
  margin: 3px !important;
  color: #efefef;
  font-family: Legendary;
  font-size: 60px;
}
</style>