<script setup>
import myPerson from './components/myPerson.vue'
import headBar from './components/headBar.vue'
</script>
<script>
export default {
  name: 'homeVue',
  data() {
    return {
      greenting: [
          'Me chamo Sávio Haistem, tenho 21 anos, estudo programação desde os 18 anos, quando ',
          'descobri que era a minha paixão. Desde criança sempre fui muito curioso em relação á ',
          'tecnologias, então essa curiosidade naturalmente me levou um dia á me perguntar como são ',
          'criados aplicativos ( mobiles ) o que me fez querer aprender a criar o meu próprio, ',
          'futuramente ao iniciar a busca por qual carreira eu deveria seguir eu não tive mais ',
          'dúvidas, serei programador.'
      ]
    }
  }
}
</script>
<template>
  <section class="home">
    <header>
      <headBar name="Savio Haistem" />
    </header>
    <main class="home-main">
      <myPerson />
      <p class="magic-description" v-text="greenting.join('')"></p>
    </main>
  </section>
</template>
<style scoped>
section > header {
  width: 100%;
}
section.home {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
}
header {
  flex-basis: 100vw;
}
main.home-main {
  display: flex;
  overflow: scroll;
  align-items: center;
  justify-content: center;
  height: calc(100vh - 6.1rem);
}
main > p.magic-description {
  margin: auto 0px;
  padding: 0px 4rem;
  overflow: scroll;
  color: #efefef;
  text-align: center;
  font-size: 20px;
  line-height: 1.8rem;
  max-width: 35rem;
  font-family: josefin;
}
@media screen and (max-width: 664px) {
  main.home-main {
    align-items: start;
  }
  main > p.magic-description {
    margin: 6rem 0px;
    font-size: 18px;
    max-height: 50vh;
  }
}
</style>
