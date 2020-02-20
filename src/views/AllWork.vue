<template>
  <div>
    <v-container fluid class="project-list">
      <v-row>
        <v-col cols="12">
          <v-row :align="alignment" :justify="justify"> 
          <ProjectItem class="project-item"
            v-for="project in projects"
            :key="project.name"
            :project="project"
          />
        </v-row>
        </v-col>
      </v-row>
    </v-container>
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
        projects: store.projects,
        alignment: "start",
        justify: "start"
      };
    }
  };
</script>

<style scoped>

.project-list{
  margin-top: -15em;
  margin-left: 25em;
}
</style>
