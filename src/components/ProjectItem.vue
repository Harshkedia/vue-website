<template>
  <div>
    <router-link :to="{ name: 'Project', params: { name: project.name } }" class="project-item">
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
  .project-item{
    padding: 2em;
    text-decoration: none;
  }
  .project-image {
    width: 15em;
    height: 15em;
    object-fit: cover;
    border-radius: 200px;
    align-self: auto;
  }

  .project-title {
    color: black;
    text-decoration: none;
    background-color: white;
    text-align: center;
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
