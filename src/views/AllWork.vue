<template>
  <div class="projects">
    <ProjectItem
      v-for="project in projects"
      :key="project.name"
      :project="project"
    />
  </div>
</template>

<script>
  // @ is an alias to /src
  import ProjectItem from "@/components/ProjectItem.vue";
  import store from "@/store.js";

  export default {
    name: "AllWork",
    components: {
      ProjectItem
    },
    data() {
      return {
        projects: store.projects
      };
    }
  };
</script>

<style scoped>
  .projects {
    display: grid;
    position: absolute;
    margin-left: 350px;
    margin-top: 30px;
    grid-row-gap: 75px;
    grid-column-gap: 75px;
    grid-template-columns: 250px 250px 250px;
  }
</style>
