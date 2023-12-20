<template>
  <main class="projects-body">
    <ul class="projects-list">
      <li v-for="(project, index) in projects" :key="index" class="project-item">
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
export default {
  name: 'projectsPage',
  data() {
    return {
      projects: Jsondata.list,
      techsVisibility: true,
      techNameVisibility: true,
      techNameIndex: null,
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
  align-items: center;
  width: 100%;
  height: 100%;
}

.projects-body > ul.projects-list {
  border: 1px solid red;
  margin: auto;
  list-style: none;
  padding: 2rem;
  width: 80vw;
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(18rem, 1fr));
  grid-auto-rows: 22rem;
  grid-auto-flow: row;
  justify-items: center;
  justify-content: center;
  align-items: center;
}
ul.projects-list > li.project-item {
  font-size: 15px;
  border: 1px solid white;
  overflow: hidden;
  width: 17rem;
  height: 21rem;
  cursor: pointer;
  background-color: #484848;
  border: 1px solid gray;
  border-radius: 8px;
}
ul.projects-list > li.project-item:hover {
  box-shadow: 0px 0px 60px 0px rgba(0, 3, 3, 0.747);
  width: calc(100% + 2rem);
  height: calc(100% + 2rem);
  z-index: 1;
}
ul.projects-list > li.project-item > div.project-info {
  color: rgb(205, 223, 255);
  padding: 0px 1.5rem;
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
    border: 1px solid rgb(255, 255, 255);
    margin: auto;
    list-style: none;
    padding: 2rem;
    width: 80vw;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(17rem, 18rem));
    grid-auto-rows: 21rem;
    grid-auto-flow: row;
    justify-items: center;
    justify-content: center;
  }

  ul.projects-list > li.project-item {
    font-size: 14px;
    border: 1px solid white;
    overflow: hidden;
    width: 17rem;
    height: 20rem;
    cursor: pointer;
    background-color: #484848;
    border: 1px solid gray;
    border-radius: 8px;
  }
  ul.projects-list > li.project-item:hover {
    box-shadow: 0px 0px 60px 0px rgba(0, 3, 3, 0.747);
    width: calc(100% + 1rem);
    height: calc(100% + 1rem);
  }
}

@media only screen and (max-width: 1107px) {
  .projects-body > ul.projects-list {
    border: 1px solid blue;
    overflow: scroll;
    list-style: none;
    padding: 2rem;
    width: 80vw;
    height: 80vh;
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(14rem, 15rem));
    grid-auto-rows: 21rem;
    grid-auto-flow: row;
  }
  ul.projects-list > li.project-item {
    font-size: 12px;
    width: 14rem;
    height: 20rem;
  }
  ul.projects-list > li.project-item:hover {
    font-size: 12px;
    width: calc(14rem + 2rem);
    height: calc(20rem + 2rem);
  }
}

@media only screen and (max-width: 418px) {
  .projects-body > ul.projects-list {
    border: 1px solid greenyellow;
    overflow: scroll;
    padding: 0px;
    padding-bottom: 5rem;
    padding-top: 5rem;
    max-height: 70vh;
    width: 100vw;
    min-width: auto;
    max-width: auto;
    grid-template-columns: repeat(auto-fill, minmax(14rem, 1fr));
    grid-gap: 0px;
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
