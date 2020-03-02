<template>
  <div id="app">
    <v-app>
      <SideBar class="sidebar"></SideBar>
      <div class="projects"><router-view /></div>
    </v-app>
  </div>
</template>

<script>
import SideBar from "@/components/SideBar.vue";
export default {
  name: "App",
  components: { SideBar }
};
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  font-family: "Courier New", Courier, monospace;
}

.sidebar {
  width: 10em;
}

.projects {
  float: left;
  width: 80%;
}
</style>
