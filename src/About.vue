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

        </h5>
      </div>
    </main>
  </section>
</template>
<style>
section.about {
  border: 1px solid red;
  width: 100%;
}
section > main.main-about {
  display: flex;
  flex-direction: row;
  border: 2px solid skyblue;
  align-items: center;
  justify-content: center;
  height: calc(100% - 6.1rem);
}

section.about > main.main-about > div.photo {
  border: 2px solid lime;
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
  border: 2px solid rgb(255, 238, 0);
  height: 30rem;
  width: 50vw;
}
@media screen and (max-width: 1150px) {
  section.about > main.main-about > div.photo > img.my-photo {
    width: 10rem;
    height: 10rem;
  }
  section.about > main.main-about > div.photo {
    height: 13rem;
    width: 100%;
  }
  section > main.main-about {
    flex-direction: column;
  }
  section.about > main.main-about > div > h5.description {
    height: 40vh;
  }
}
</style>