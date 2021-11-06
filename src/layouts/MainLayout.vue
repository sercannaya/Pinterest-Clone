<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer app permanent>
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            <v-layout align-center>
              <v-img 
                width="10"
                lazy-src="https://logos-world.net/wp-content/uploads/2020/09/Pinterest-Logo-2011-present.png" 
                src="https://logos-world.net/wp-content/uploads/2020/09/Pinterest-Logo-2011-present.png" 
              />
              Pinterest 
            </v-layout>
              
          </v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <div class="mx-4 subtitle-2 grey--text">Insights</div>
      <v-list dense nav >
        <v-list-item link >
          <v-list-item-icon>
            <v-icon> mdi-mail </v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title> Messages </v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-list-item link >
          <v-list-item-icon>
            <v-icon> mdi-bell </v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title> Notifications </v-list-item-title>
          </v-list-item-content>
          <v-list-item-avatar size="25" color="orange" class="white--text subtitle-2"> 2 </v-list-item-avatar>
        </v-list-item>
        
      </v-list>
    </v-navigation-drawer>

    <v-main>
        <home-page />
    </v-main>
  </v-app>
</template>

<script>
import HomePage from '@/pages/HomePage.vue';

export default {
    components: {
        HomePage,
    },
    data() {
        return {
            items: [
                { title: 'Home', icon: 'mdi-view-dashboard' },
                { title: 'Recent', icon: 'mdi-image' },
                { title: 'Following', icon: 'mdi-help-box' },
            ],
            items2: [
                { title: 'Messages', icon: 'mdi-view-dashboard' },
                { title: 'Notification', icon: 'mdi-image' },
            ],
            
        }
    },
};
</script>

<style>
/*  */
</style>