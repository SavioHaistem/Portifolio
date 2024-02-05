<script>
export default {
  name: 'headBar',
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
  color: #7cfff8;
  padding: 0px 0.5rem;
  font-family: runes;
  font-size: 30px;
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
  font-family: blkchcry;
  font-size: 60px;
  animation: textlight 5s infinite steps(120);
}

@keyframes textlight {
  from, to { text-shadow: 1px 2px 40px rgb(0, 188, 209); }
  50% { text-shadow: 1px 2px 70px rgb(0, 229, 255);}
}
@media screen and (max-width: 428px) {
  p.rune {
    transform: translateY(-20px);
  }
  p.user-name {
    font-size: 40px;
  }
  @media screen and (max-width: 664px) {
  }
}
</style>
