<script setup>
import headBar from './components/headBar.vue';
</script>
<script>
export default {
  name: "aboutVue"
} 
</script>
<template>
  <section class="about">
    <headBar name="Savio Haistem" />
    <main class="main-about">
      <div class="photo">
        <img src="../public/images/1687661964157.jpg" alt="my-photo" class="my-photo" />
      </div>
      <div>
        <h5 class="description">
          Me chamo Sávio Haistem, tenho 21 anos, estudo programação desde os 18 anos, quando descobri que era a minha paixão.
          Desde criança sempre fui muito curioso em relação á tecnologias, então essa curiosidade naturalmente me levou um dia
          á me perguntar como são criados aplicativos ( mobiles ) o que me fez querer aprender a criar o meu próprio, futuramente
          ao iniciar a busca por qual carreira eu deveria seguir eu não tive mais dúvidas, serei programador.
        </h5>
      </div>
    </main>
  </section>
</template>
<style>
section.about {
  width: 100%;
}
section > main.main-about {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  height: calc(100% - 6.1rem);
}
 
section.about > main.main-about > div.photo {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 20rem;
  height: 100%;
}
section.about > main.main-about > div.photo > img.my-photo {
  width: 15rem;
  height: 15rem;
  border-radius: 100%;
  box-shadow: 0px 0px 70px 0px white;
}

section.about > main.main-about > div > h5.description {
  border: 1px solid red;
  font-family: josefin;
  font-size: 17px;
  line-height: 1.8rem;
  padding: 2rem 5rem;
  height: 14rem;
  overflow: scroll;
  max-width: 30rem;
}
@media screen and (max-width: 1150px) {
  section.about > main.main-about > div.photo > img.my-photo {
    width: 10rem;
    height: 10rem;
  }
  section.about > main.main-about > div.photo {
    height: 12rem;
  }
  section > main.main-about {
    flex-direction: column;
  }
  section.about > main.main-about > div > h5.description {
  }
}
</style>