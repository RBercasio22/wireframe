<template>
    <v-app id="inspire"
    >
      <v-navigation-drawer
       v-model="drawer"
       app
       >
       
        <SideNav />
      </v-navigation-drawer>
  
      <v-app-bar
      color="#ffbf00"
      >
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
  
        <v-app-bar-title style="color: white; font-weight: 500;">
          <v-icon
          icon="mdi-cart"
          class="ma-2 fixed-position"
          color="black"

          >
          </v-icon>
          SAMPLE APPLICATION</v-app-bar-title>
      </v-app-bar>
  
      <v-main>
       
        <fixed-logo />
        <app-footer />
      </v-main>
    </v-app>
  </template>
  
  <script setup>
    import { ref } from 'vue'
    import FixedLogo from './FixedLogo.vue'
  
    const drawer = ref(null)
  </script>
  
  <script>
    export default {
  components: { FixedLogo },
      data: () => ({ drawer: null }),
    }
  </script>