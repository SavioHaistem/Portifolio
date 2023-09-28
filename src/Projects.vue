<template>
  <main class="projects-body">
    <li class="projects-list">
      <ul v-for="(project, index) in projects" :key="index" class="project-item">
        <img :src="project.image" alt="">
        <p>{{ project.name }}</p>
        <p>{{ project.description }}</p>
      </ul>
    </li>
  </main>
</template>

<script>
import Jsondata from "@/assets/projects/projects.json"
export default {
  name: 'projectsPage',
  data() {
    return {
      projects: Jsondata.list,
    }
  },
  mounted() {
    console.log(this.projects)
  }
}
</script>

<style scoped>
main.projects-body {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid red;
  width: 100%;
  height: 28rem;
  margin: auto 5rem auto 0px;
}

.projects-body > li.projects-list {
   list-style: none;
   border: 1px solid cyan;
   overflow: auto;
   width: 90vw;
   height: calc(28rem - 6rem);
   display: grid;
   justify-items: center;
   grid-gap: 1rem;
   grid-template-columns: repeat(auto-fill, minmax(15rem, 1fr));
   grid-auto-rows: 20rem;
   grid-auto-flow: row;
}
li.projects-list > ul.project-item {
  background-image: url();
   border: 1px solid greenyellow;
   height: 100%;
   width: 13rem;
}
</style>
