<template>
  <div id="app">
    <v-app>
      <v-card width="300" class="side-bar" elevation="0" outline="false">
        <v-navigation-drawer permanent>
          <v-list-item  class="display-1"><router-link to="/" id="side-bar-header">Harshvardhan<br> Kedia</router-link></v-list-item>
          <v-list dense nav class="links">
            <v-list-item><router-link to="/all-work" id="side-bar-item">All Work</router-link></v-list-item>
            <v-list-item><router-link to="/about" id="side-bar-item">Design Computing</router-link></v-list-item>
            <v-list-item><router-link to="/about" id="side-bar-item">Architecture</router-link></v-list-item>
            <v-list-item><router-link to="/about" id="side-bar-item">Computational Art</router-link></v-list-item>
            <v-list-item><router-link to="/about" id="side-bar-item">Ideas</router-link></v-list-item>
            <v-list-item><router-link to="/about" id="side-bar-item-2">About</router-link></v-list-item>
            <v-list-item><router-link to="/about" id="side-bar-item-2">Resume</router-link></v-list-item>
          </v-list>
        </v-navigation-drawer>
      </v-card>
      <router-view/>
    </v-app>
  </div>
</template>

<script>
export default {
  name: 'App',
}

</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
}

.links {
  margin-top: 1em;
}

.side-bar{
  margin-top: 1em;
  margin-left: .5em;
}

#side-bar-header {
  font-weight: bold;
  color: red;
  text-decoration: none;
  line-height: 1;
  margin-top: .5em;
}

#side-bar-header:hover{
  color:black;
}

#side-bar-item {
  color: #000000;
  text-decoration: none;
  line-height: 1;
}

#side-bar-item:hover{
  color: rgb(255, 0, 0);
}

#side-bar-item-2 {
  color: #616060;
  text-decoration: none;
  line-height: 1;
}

#side-bar-item-2:hover{
  color: black;
}
</style>