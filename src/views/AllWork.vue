<template>
  <div>
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <v-row>
            <ProjectItem
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
      alignment: "end",
      justify: "center"
    };
  }
};
</script>

<style scoped></style>
