<template>
  <div id="app">
    <div id="side-bar">
      <li><router-link to="/" id="side-bar-header">Harshvardhan Kedia</router-link></li>
      <li><router-link to="/all-work" id="side-bar-item">All Work</router-link></li>
      <li><router-link to="/about" id="side-bar-item">Design Computing</router-link></li>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#side-bar {
  position: fixed;
  z-index: +1;
  margin-top: 1em;
  margin-left: 2em;
  height: 30em;
  width: 15em;
  background-color: rgb(255, 255, 255);
  list-style-type: none;
  line-height: 2;
  text-align: left;
}

#side-bar-header {
  font-size: 2em;
  font-weight: bold;
  color: #aa3939;
  text-decoration: none;
  line-height: 1;
}

#side-bar-item {
  font-size: 10pt;
  color: #000000;
  font-size: 1em;
  text-decoration: none;
  line-height: 1;
}

#app {
  font-family: Helvetica;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
