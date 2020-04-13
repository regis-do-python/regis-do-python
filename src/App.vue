<template>
  <v-app>
    <v-app-bar
      app
      color="#092e20"
      dark
    >
      <div class="d-flex align-center">
        <!-- <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        /> -->
        <span><i class="fa fa-youtube-play fa-2x"></i></span>
        <h2 class="ml-5">Regis do Python</h2>

      </div>

      <v-row
        align="center"
        class="ml-10"
        style="max-width: 650px"
      >
        <v-text-field
          :append-icon-cb="() => {}"
          v-model="search"
          placeholder="Search..."
          outlined
          append-icon="mdi-magnify"
          color="white"
          hide-details
        />
      </v-row>

    </v-app-bar>

    <v-content>
      <Videos :search="search"/>
    </v-content>
  </v-app>
</template>

<script>
import Videos from './components/Videos';

export default {
  name: 'App',

  components: {
    Videos,
  },

  data: () => ({
    'search': ''
  }),
};
</script>
