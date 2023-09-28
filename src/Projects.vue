<template>
  <main class="projects-body">
    <ul class="projects-list">
      <li
        v-for="(project, index) in projects"
        :key="index"
        class="project-item"
        @mouseover="changeVisibility((elementHovered = index))"
        @mouseout="changeVisibility((elementHovered = null))"
      >
        <img :src="project.image" :alt="project.name" class="project-image" />
        <div class="project-techs" v-show="techsVisibility && elementHovered == index" :key="index">
          <img
            class="project-tecnologie"
            v-for="(tech, index) in project.tecnologias"
            :key="index"
            :src="'../src/assets/images/tecnologies/' + tech + '.png'"
          />
          <p>{{ tech }}</p>
        </div>
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
export default {
  name: 'projectsPage',
  data() {
    return {
      projects: Jsondata.list,
      techsVisibility: true,
      elementHovered: null
    }
  },
  mounted() {
    console.log(this.projects)
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
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 28rem;
  margin: auto 5rem auto 0px;
}

.projects-body > ul.projects-list {
  list-style: none;
  padding: 2rem;
  overflow: auto;
  width: 80vw;
  height: 30rem;
  display: grid;
  grid-gap: 2rem;
  grid-template-columns: repeat(auto-fill, minmax(15rem, 1fr));
  grid-auto-rows: 20rem;
  grid-auto-flow: row;
}
ul.projects-list > li.project-item {
  overflow: hidden;
  background-color: #484848;
  border: 1px solid #626262;
  border-radius: 8px;
}
ul.projects-list > li.project-item:hover {
  box-shadow: 0px 0px 30px 0px rgba(166, 255, 251, 0.236);
}
ul.projects-list > li.project-item > div.project-techs {
  transform: translateY(-101px);
  overflow: auto;
  margin-bottom: -96px;
  display: flex;
  gap: 5px;
  padding-left: 20px;
  align-items: flex-end;
  height: 6rem;
  width: 100%;
  background-image: linear-gradient(to top, rgba(0, 0, 0, 0.589), rgba(80, 80, 80, 0));
  transition: 0.3s;
  animation: background-up;
}
ul.projects-list > li.project-item > div.project-techs > img.project-tecnologie {
  background-color: white;
  border-radius: 10px;
  padding: 5px;
  height: 19px;
  width: 19px;
  margin-bottom: 10px;
}
ul.projects-list > li.project-item > div.project-info {
  color: rgb(205, 223, 255);
  padding: 0px 2rem;
}
ul.projects-list > li.project-item > div.project-info > p.project-description {
  overflow: auto;
  height: 5rem;
}
ul.projects-list > li.project-item > img.project-image {
  width: 100%;
  height: 10rem;
  object-fit: cover;
  border-radius: 8px 8px 0px 0px;
  overflow: hidden;
}
</style>
