<script setup>
import myPerson from './components/myPerson.vue';
import navBar from './components/headBar.vue';
</script>
<script>
export default {
  name: "homeVue",
  data() {
    return {
      greenting: ['Programar é como fazer magia, você precisa pensar em uma solução para algo, ',
        'quando sabe o que deve fazer você irá tentar achar uma forma de fazer seus  pensamentos ',
        'virarem realidade, e então você começa a organizar seus feitiços, vai ler alguns grimórios ',
        'para ter certeza que está usando o melhor feitiço para  cada problema e então depois do ',
        'relógio correr incontáveis horas enquanto você  configura seus feitiços da melhor forma ',
        'que consegue a magia finalmente acontece, os computadores começarão a executar seu código ',
        'e todas as regras que você pensou e irão fazer algo acontecer. O mundo moderno está cheio ',
        'de magos programadores, feitiços tecnológicos.'],
    }
  },
}
</script>
<template>
  <section class="home">
    <header>
      <navBar class="nav" name="Savio Haistem" />
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
  padding: 2rem 4rem;
  overflow: scroll;
  color: #efefef;
  text-align: center;
  font-size: 20px;
  height: 20rem;
  max-width: 35rem;
  font-family: josefin;
}
@media screen and (max-width: 664px) {
  main.home-main {
    align-items: start;
  }
  main > p.magic-description {
    font-size: 18px;
    max-height: 16rem;
  }
}
</style>