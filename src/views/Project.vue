<template>
  <div class="project">
    <h2 class="project-title">{{project.name}}</h2>
    <h2 class="project-subtitle">{{project.description}}</h2>
  </div>
</template>

<script>
// @ is an alias to /src
import store from '@/store.js'

export default {
  name: 'Project',
  components: {
  },
  data (){
    return {
      name: this.$route.params.name
    }
  },
  computed: {
    project(){
      return store.projects.find(
        project => project.name === this.name
      )
    }
  }
}
</script>

<style scoped>
.project {
  display: grid;
  position: absolute;
  margin-left: 350px;
  margin-top: 60px;
  grid-column-gap: 50px;
  grid-template-columns: 450px 450px;
  justify-content: left;  
  align-items: center;
  background-color: white;
}

.project-title{
  position: absolute;
  float: left;
  font-size: 18pt;
  font-weight: normal;
  color: black;
}

.project-subtitle{
  position: absolute;
  margin-top: 4em;
  float: left;
  font-size: 10pt;
  color: gray;
  font-weight: normal;
}
</style>
