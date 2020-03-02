<template>
  <div class="project">
    <div class="title">
      <div class="project-title">{{ project.name }}</div>
      <div class="project-subtitle">{{ project.description }}</div>
      <br />
      <div class="description">
        <b>When</b>: {{ project.when }} <br />
        <Collaborators :collaborators="project.with"></Collaborators>
        <b>Role</b>: {{ project.role }} <br />
        <b>What</b>: {{ project.what }} <br />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import store from "@/store.js";
import Collaborators from "@/components/Collaborators.vue";

export default {
  name: "Project",
  components: {
    Collaborators
  },
  data() {
    return {
      name: this.$route.params.name
    };
  },
  computed: {
    project() {
      return store.projects.find(project => project.name === this.name);
    }
  }
};
</script>

<style scoped>
.title {
  margin-left: 18em;
  margin-top: -20em;
}

.project-title {
  color: black;
  font-size: 1.5em;
}

.project-subtitle {
  color: gray;
  font-size: 0.8em;
}

.description {
  color: black;
  font-size: 0.75em;
  margin-right: 5em;
  text-decoration: none;
}
</style>
