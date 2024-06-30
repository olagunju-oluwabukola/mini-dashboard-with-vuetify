
<template>
  <v-card>
    <v-layout>
      <v-app-bar
        color="purple-darken-3"
        prominent
        
      >
        <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer" ></v-app-bar-nav-icon>
        <v-toolbar-title>EdRead</v-toolbar-title>
        <v-spacer></v-spacer>

        <!-- <template v-if="$vuetify.display.mdAndUp" >
          <v-btn icon="mdi-magnify" variant="text">hhh</v-btn>

          <v-btn icon="mdi-filter" variant="text">jjj</v-btn>
        </template> -->

        <v-btn icon="mdi-dots-vertical" variant="text" class="text-lowercase mr-8">
        Log in
        </v-btn>
      </v-app-bar>

      <v-navigation-drawer
        v-model="drawer"
        :location="$vuetify.display.mobile ? 'left' : undefined"
        temporary 
        class="primary"
      >
        <v-list
          :items="items"
          v-for="item in items" :key="item.route" 
         
          @click="$router.push({path: item.route})"
        >
        <v-list-item-title>
          <v-list-tile-content>
            <v-icon class="red-text" >{{item.icon }}</v-icon>
            <v-list-tile-title> {{ item.text }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-item-title>
      </v-list>
      </v-navigation-drawer>

      

     
        <v-card-text>
          <router-view></router-view>
        </v-card-text>
     
    </v-layout>
  </v-card>
<login/>
</template>
<script>
// import { RouterLink, RouterView } from 'vue-router'
  export default {
    data: () => ({
      drawer: false,
      group: null,
      items: [
        {
          icon: 'dashboard',
          text: 'Dashboard',
          route: '/dashboard'
          
        },
        {
         icon: 'folder',
          text: 'curriculum',
          route: '/curriculum'
        },
        {
          icon: 'team',
          text: 'Team',
          route: '/team'
        },
        
      ],
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
  }
</script>

<style scoped>

</style>




