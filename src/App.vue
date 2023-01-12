<template  >
  <v-app  class="inspire">
    <v-navigation-drawer class="amber lighten-5" v-model="drawer" app>
     <v-list-item color="teal lighten-2">
      <v-list-item-content>
        <v-list-item-title >
         
        </v-list-item-title>
        <v-list-item-subtitle class="d-block pa-2 teal lighten-3 white--text">
            Add You Important learnings 
        </v-list-item-subtitle>
      </v-list-item-content>
     </v-list-item>
     
    <v-list dense >

      <v-list-item-group  color="teal lighten-2">
        <v-list-item  v-for="(item, i) in items" :key="i" :to="item.link" link>
          <v-list-item-icon>
            <v-icon v-text="item.icon"></v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title v-text="item.title"></v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>

    </v-navigation-drawer>

    <v-app-bar app class="   teal darken-2   white--text">
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title class="  text-center">BOOK MEMORY</v-toolbar-title>
    </v-app-bar>

    <v-main>
    <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: null,
    items: [
      { title: "Home", icon: "mdi-home", link:"/" },
      { title: "Add Post", icon: "mdi-note-plus", link: "/add-post" },
      { title: "About", icon: "mdi-help-box", link: "/about" },
    ]
  }),
 
}
</script>