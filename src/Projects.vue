<template>
  <main class="projects-body">
    <ul class="projects-list">
      <li
        v-for="(project, index) in projects"
        :key="index"
        class="project-item"
        @click="openProject(project.link)"
      >
        <img :src="project.image" :alt="project.name" class="project-image" />
        <div class="project-info">
          <h3 class="project-name">{{ project.name }}</h3>
          <p class="project-description">{{ project.description }}</p>
        </div>
      </li>
    </ul>
  </main>
</template>

<script>
import Jsondata from '@/assets/projects/projects.json'
import { useLink } from 'vue-router';
export default {
  name: 'projectsPage',
  data() {
    return {
      projects: Jsondata.list
    }
  },
  methods: {
    openProject(link) {
      useLink.router.push(link)
    }
  }
}
</script>
<style scoped>
* {
  font-family: josefin;
}
*::-webkit-scrollbar {
  display: none;
}

@keyframes background-up {
  0% {
    background-image: linear-gradient(to top, rgba(0, 0, 0, 0.105), rgba(80, 80, 80, 0));
  }
  50% {
    background-image: linear-gradient(to top, rgba(0, 0, 0, 0.4), rgba(80, 80, 80, 0));
  }
  100% {
    background-image: linear-gradient(to top, black, rgba(80, 80, 80, 0));
  }
}
main.projects-body {
  display: flex;
  align-items: center;
  width: 100%;
  height: 100%;
}

.projects-body > ul.projects-list {
  overflow: scroll;
  margin: auto;
  padding: 5rem;
  list-style: none;
  max-width: 70vw;
  display: grid;
  max-height: 70vh;
  grid-template-columns: repeat(auto-fit, minmax(18rem, 1fr));
  grid-auto-rows: 22rem;
  grid-auto-flow: row;
  justify-items: center;
  justify-content: center;
  align-items: center;
}
ul.projects-list > li.project-item {
  font-size: 15px;
  border: 1px solid rgba(160, 160, 160, 0.308);
  overflow: hidden;
  width: 17rem;
  height: 21rem;
  cursor: pointer;
  background-color: #4e415c;
  border: 1px solid rgba(255, 255, 255, 0.356);
  border-radius: 8px;
}
ul.projects-list > li.project-item:hover {
  box-shadow: 0px 0px 60px 0px rgba(0, 3, 3, 0.747);
  border: 2px solid white;
  width: 17.5rem;
  height: 22rem;
  z-index: 1;
}
ul.projects-list > li.project-item > div.project-info {
  color: rgb(214, 254, 255);
  padding: 0px 1.5rem;
  max-height: fit-content;
}
ul.projects-list > li.project-item > div.project-info > p.project-description {
  color: white;
  overflow: auto;
  height: 6rem;
}
ul.projects-list > li.project-item > img.project-image {
  width: 100%;
  height: 10rem;
  object-fit: cover;
  border-radius: 8px 8px 0px 0px;
  overflow: hidden;
}

@media screen and (max-width: 1436px) {
  .projects-body > ul.projects-list {
    width: 80vw;
    grid-template-columns: repeat(auto-fill, minmax(17rem, 18rem));
    grid-auto-rows: 21rem;
  }

  ul.projects-list > li.project-item {
    font-size: 14px;
    width: 17rem;
    height: 20rem;
  }
  ul.projects-list > li.project-item:hover {
    width: calc(100% + 1rem);
    height: calc(100% + 1rem);
  }
}

@media only screen and (max-width: 1107px) {
  .projects-body > ul.projects-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(14rem, 15rem));
    grid-auto-rows: 21rem;
  }
  ul.projects-list > li.project-item {
    font-size: 12px;
    width: 14rem;
    height: 20rem;
  }
  ul.projects-list > li.project-item:hover {
    width: calc(14rem + 2rem);
    height: calc(20rem + 2rem);
  }
}

@media only screen and (max-width: 418px) {
  .projects-body > ul.projects-list {
    grid-template-columns: repeat(auto-fill, minmax(14rem, 1fr));
    grid-auto-rows: 22rem;
  }
  ul.projects-list > li.project-item {
    font-size: 12px;
    width: 13rem;
    height: 20rem;
  }
  ul.projects-list > li.project-item:hover {
    width: 15.5rem;
    height: 22.5rem;
  }
}
</style>
