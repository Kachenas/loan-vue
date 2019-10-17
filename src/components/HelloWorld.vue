<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
      clipped
    >
      <v-list dense>
        <v-list-item>
          <v-list-item-action>
            <v-icon>mdi-view-dashboard</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <router-link class="nav-link" to="/about">
            <v-list-item-title>About</v-list-item-title>
            </router-link>
          </v-list-item-content>
        </v-list-item>
        <v-list-item>
          <v-list-item-action>
            <v-icon>mdi-cellphone</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <router-link class="nav-link" to="/contact">
            <v-list-item-title>Contact Us</v-list-item-title>
             </router-link>
          </v-list-item-content>
        </v-list-item>
        <v-list-item>
        <v-list-item-action>
            <v-icon>mdi-account-supervisor-circle</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <router-link class="nav-link" to="/register">
            <v-list-item-title>Register</v-list-item-title>
             </router-link>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar
      app
      clipped-left
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>Ecommerce</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <v-container
        class="fill-height"
        fluid
      >
        <v-row
          align="center"
          justify="center"
        >
        </v-row>
      </v-container>
    </v-content>

    <v-footer app>
      <span>&copy; 2019</span>
    </v-footer>
  </v-app>
</template>

<script>



  export default {
    props: {
      source: String,
    },
    data: () => ({
      drawer: null,
    }),
    created () {
      this.$vuetify.theme.dark = true
    },
  }
</script>