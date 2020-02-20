<template>
  <div class="project-item">
    <router-link :to="{ name: 'Project', params: { name: project.name } }">
      <img
        class="project-image"
        :src="require('@/assets/' + project.image)"
        :alt="project.name"
      />
      <div class="project-title">{{ project.name }}</div>
      <div class="project-subtitle">{{ project.description }}</div>
    </router-link>
  </div>
</template>

<script>
  export default {
    name: "ProjectItem",
    props: ["project"]
  };
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .project-image {
    width: 250px;
    height: 250px;
    object-fit: cover;
    border-radius: 200px;
  }

  .project-title {
    color: black;
    text-decoration: none;
    background-color: white;
  }

  .project-subtitle {
    font-family: "Work Sans", sans-serif;
    color: gray;
    font-weight: normal;
    text-decoration: none;
    font-size: 8pt;
    text-align: center;
    margin-top: 5px;
  }
</style>
