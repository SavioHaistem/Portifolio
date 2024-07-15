<script setup>
import headBar from './components/headBar.vue'
</script>
<script>
import { library } from '@fortawesome/fontawesome-svg-core'
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faWhatsapp, faGithub, faLinkedin, faInstagram } from '@fortawesome/free-brands-svg-icons'
library.add(faWhatsapp, faGithub, faLinkedin, faInstagram)

export default {
  name: 'aboutPage',
  components: {
    FontAwesomeIcon
  }
}
</script>
<template>
  <section class="about">
    <headBar name="Savio Haistem" />
    <main class="main-about">
      <div class="photo">
        <img src="../public/images/1687661964157.jpg" alt="my-photo" class="my-photo" />
      </div>
      <div class="description-body">
        <h5 class="description">
          Programar é como fazer magia, você precisa pensar em uma solução para algo, quando sabe o
          que deve fazer você irá tentar achar uma forma de fazer seus pensamentos virarem
          realidade, e então você começa a organizar seus feitiços, vai ler alguns grimórios para
          ter certeza que está usando o melhor feitiço para cada problema e então depois do relógio
          correr incontáveis horas enquanto você configura seus feitiços da melhor forma que
          consegue a magia finalmente acontece, os computadores começarão a executar seu código e
          todas as regras que você pensou e irão fazer algo acontecer. O mundo moderno está cheio de
          magos programadores, feitiços tecnológicos.
        </h5>
        <ul class="link-list">
          <a href="https://wa.me/5584999918236?text=Oi%20Sávio" class="link-item">
            <font-awesome-icon :icon="['fab', 'fa-whatsapp']" class="link-icon whatsap" />
          </a>
          <a href="https://github.com/SavioHaistem" class="link-item">
            <font-awesome-icon :icon="['fab', 'fa-github']" class="link-icon whatsap" />
          </a>
          <a href="https://www.linkedin.com/in/saviohaistem/" class="link-item">
            <font-awesome-icon :icon="['fab', 'fa-linkedin']" class="link-icon whatsap" />
          </a>
          <a href="https://www.instagram.com/saviohaistem/" class="link-item">
            <font-awesome-icon :icon="['fab', 'fa-instagram']" class="link-icon whatsap" />
          </a>
        </ul>
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

section > main.main-about > div.description-body {
  display: flex;
  flex-direction: column;
  align-items: center;
}

div.description-body > ul.link-list {
  display: flex;
  justify-content: center;
  gap: 5px;
  width: 14rem;
  margin: 1rem 0px;
  padding: 0px;
}

div.description-body > ul.link-list > .link-item {
  display: flex;
  justify-content: center;
  align-items: center;
  color: rgb(61, 61, 61);
  font-size: 20px;
  background-color: #d4fffb;
  border-radius: 100%;
  box-shadow: 0px 0px 20px 0px #d4fffb;
  margin: 0px 0px 0px 2px;
  height: 35px;
  width: 35px;
}

ul.link-list > .link-item > .link-icon {
  margin: 0px 0px 0px 2px;
}

section.about > main.main-about > div.photo {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 20rem;
}
section.about > main.main-about > div.photo > img.my-photo {
  width: 15rem;
  height: 15rem;
  border-radius: 8rem;
  border: 5px solid rgb(232, 212, 255);
  box-shadow: 0px 0px 240px 0px rgba(232, 212, 255, 0.678);
  animation: boxlight 10s infinite steps(80);
}

section.about > main.main-about > div > h5.description {
  font-family: josefin;
  text-align: center;
  font-size: 18px;
  line-height: 1.8rem;
  padding: 1rem 3rem;
  overflow: scroll;
  max-width: 35rem;
  margin: 0px;
}
@keyframes boxlight {
  from,
  to {
    box-shadow: 0px 0px 80px 0px rgba(232, 212, 255, 0.418);
  }
  50% {
    box-shadow: 0px 0px 100px 0px rgba(232, 212, 255, 0.5);
  }
}

@media screen and (max-width: 1150px) {
  section.about > main.main-about > div.photo > img.my-photo {
    width: 8rem;
    height: 8rem;
  }
  section.about > main.main-about > div.photo {
    height: 12rem;
  }
  section > main.main-about {
    flex-direction: column;
  }
  section.about > main.main-about > div > h5.description {
    font-size: 15px;
    line-height: 1.3rem;
    max-width: 70vw;
  }

  @media screen and (max-width: 770px) {
    section > main.main-about {
      margin-top: 2rem;
      justify-content: start;
    }
  }
}
</style>
