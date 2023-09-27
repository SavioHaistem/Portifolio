<!-- eslint-disable vue/no-unused-components -->
<script>
import Home from './Home.vue';
import About from './About.vue';
import { library } from '@fortawesome/fontawesome-svg-core';
import { faHatWizard } from '@fortawesome/free-solid-svg-icons'
import { faGripfire } from "@fortawesome/free-brands-svg-icons"
import { faBookQuran } from '@fortawesome/free-solid-svg-icons';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import Projects from './Projects.vue';

library.add(faHatWizard, faGripfire, faBookQuran)
export default {
  components: {
    Home,
    About,
    Projects,
    FontAwesomeIcon
  },
  data() {
    return {
      currentTab: 'Home',
      tabs: ['Home', 'About', 'Projects'],
      icons: ['fa-brands fa-gripfire', 'fa-solid fa-hat-wizard', 'fa-solid fa-book-quran'],
      IconsColors: ['rgb(107, 228, 255)', '#FFFF00', '#FF78D4'],
      IconsShadow: ['#A9FFFF','#FFFCA1','#e1a1bf']
    }
  }
}
</script>

<template>
  <section class="back">
    <nav class="nav-bar">
      <button
        v-for="(tab, index) in tabs"
        :key="tab"
        @click="currentTab = tab"
        :class="['nav-button', { active: currentTab === tab }, currentTab]"
        :style="currentTab === tab ? { boxShadow: '0px 0px 18px 0px ' + IconsShadow[index] } : {}"
      >
        <font-awesome-icon
          :icon="icons[index]"
          :class="['tab-icon', tabs[index]]"
          :style="currentTab === tab ? { color: IconsColors[index] } : {color:'#2e2e2e'}"
        />
      </button>
    </nav>
    <component :is="currentTab"></component>
  </section>
</template>
<style>
* {
  transition: 0.2s;
}
*::-webkit-scrollbar {
  display: none;
}
section.back {
  display: flex;
  width: 100vw;
  height: 100vh;
}
section > nav.nav-bar {
  position: absolute;
  right: 0;
  bottom: 0;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 0.5rem;
  position: absolute;
  margin-top: 50vh;
  width: 5rem;
  height: 100%;
}

section > nav button {
  transition: 0.7s all;
}

section > nav button.nav-button {
  background-color: #787878;
  border: #2e2e2e 3px solid;
  border-left: 2px solid rgb(147, 147, 147);
  border-top: 2px solid rgb(160, 160, 160);
  font-weight: bold;
  height: 3.5rem;
  width: 3rem;
  border-radius: 1.2rem;
  cursor: pointer;
}

nav > button .tab-icon {
  width: 2rem;
  height: 2rem; 
  color: black;
}

nav > button .tab-icon.About {
  width: calc(2rem - 0.4rem);
  height: calc(2rem - 0.4rem);
}
nav > button .tab-icon.Projects {
  width: calc(2rem - 0.4rem);
  height: calc(2rem - 0.4rem);
}

@media screen and (max-width: 768px) {
  section > nav.nav-bar {
    width: 100%;
    height: 5rem;
    flex-direction: row;
  }
}
@media screen and (max-width: 768px) {
  section > nav.nav-bar {
    width: 100%;
    height: 5rem;
    flex-direction: row;
  }
}
</style>