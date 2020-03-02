<template>
  <div>
    <v-container class="side-bar" floating>
      <v-card height="350" width="200">
        <v-navigation-drawer v-model="drawer" permanent>
          <v-list dense nav>
            <v-list-item two-line>Harshvardhan Kedia</v-list-item>
            <v-list-item v-for="item in items" :key="item" link>
              <v-list-item-content>
                <v-list-item-title>{{ item }}</v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-navigation-drawer>
      </v-card>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "SideBar",
  data() {
    return {
      drawer: true,
      items: [
        "All Work",
        "Design Computation",
        "Architecture",
        "Art",
        "About",
        "Resume"
      ]
    };
  },
  computed: {
    bg() {
      return this.background
        ? "https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
        : undefined;
    }
  }
};
</script>

<style scoped>
.side-bar {
  margin-top: 0.5em;
  margin-left: 0.5em;
}

#side-bar-header {
  color: red;
  text-decoration: none;
  line-height: 1;
  margin-top: 0.5em;
  margin-bottom: 0.5em;
  font-size: 2em;
}

#side-bar-item {
  color: #000000;
  text-decoration: none;
  line-height: 1;
}

#side-bar-item:hover {
  color: rgb(255, 0, 0);
}

#side-bar-item-2 {
  color: #616060;
  text-decoration: none;
  line-height: 1;
}

#side-bar-item-2:hover {
  color: black;
}

.router-link-active {
  color: red;
}
</style>
