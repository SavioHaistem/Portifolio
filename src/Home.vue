<script setup>
import myPerson from './components/myPerson.vue';
import navBar from './components/navBar.vue';
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
    <myPerson />
    <main class="home-main">
      <p class="magic-description" v-text="greenting.join('')"></p>
    </main>
  </section>
</template>
 <style scoped>
section.home {
   width: 100%;
}
main.home-main {
  display: flex;
  max-height: 40rem;
  justify-content: center;
  height: 40rem;
}
main > p.magic-description {
  color: #efefef;
  max-width: 40rem;
  font-size: 20px;
  text-align: center;
  margin: auto;
  font-family: josefin;
  line-height: 2rem;
  padding: 0 5rem;
}
</style>