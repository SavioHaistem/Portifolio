<!-- eslint-disable vue/no-unused-components -->
<script>
import Home from './Home.vue';
import About from './About.vue';
export default {
  components: {
    Home,
    About
  },
  data() {
    return {
      currentTab: 'Home',
      tabs: ['Home', 'About']
    }
  }
}
</script>

<template>
  <section class="back">
    <nav class="nav-bar">
      <button v-for="tab in tabs" :key="tab" class="nav-button" @click="currentTab = tab">{{ tab }}</button>
    </nav>
    <component :is="currentTab"></component>
  </section>
</template>
<style>
section.back {
  display: flex;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
}
section > nav.nav-bar {
  position: absolute;
  right: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 0.5rem;
  position: absolute;
  margin-top: 50vh;
  transform: translateY(-50%);
  width: 5rem;
  height: 30rem;
}
section > nav button.nav-button {
  height: 4rem;
  width: 4rem;
  border-radius: 0.5rem;
}
</style>