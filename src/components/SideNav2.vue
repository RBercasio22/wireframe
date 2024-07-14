<template>
    <v-card>
      <v-layout>
        <v-navigation-drawer
          v-model="drawer"
          color="#FAFAFA"
          theme="dark"
          permanent
          app
        >
        
          <v-list>
            <v-list-item
              v-for="item in items"
              :key="item.title"
              :prepend-icon="item.icon"
              :title="item.title"
              :class="{'v-list-item--active': item.title === activeItem}"
              @click="activateItem(item.title)"
            >
            </v-list-item>
            <div 
              class="pa-1"
              style="margin-top: 100px"

            >
                <v-btn block @click="logout">Logout</v-btn>
            </div>
        
          </v-list>
        </v-navigation-drawer>
        <v-main min-height="800px">
          <!-- Content here -->
        </v-main>
      </v-layout>
    </v-card>
  </template>
  
  <script>
  export default {
    data() {
      return {
        drawer: true, // to control the visibility of the navigation drawer
        activeItem: 'Dashboard', // default active item
        items: [
          { icon: 'mdi-view-dashboard', title: 'Dashboard' },
          { icon: 'mdi-account-box', title: 'Account' },
          { icon: 'mdi-gavel', title: 'Admin' },
        ],
      }
    },
    methods: {
      activateItem(title) {
        this.activeItem = title
      },
      logout() {
        // Implement logout functionality
      }
    }
  }
  </script>
  
  <style scoped>
  .v-list-item--active {
    background-color: #f5f5f5; /* Adjust color or style for active state */
  }
  </style>
  