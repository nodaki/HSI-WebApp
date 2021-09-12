<template>
  <v-app dark>
    <v-app-bar
      fixed
      app
    >
      <v-app-bar-title>
        {{title}}
      </v-app-bar-title>
      <v-spacer></v-spacer>
      <v-btn v-if="this.$auth.loggedIn" outlined @click="logout">
        Sing out
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      title: 'App'
    }
  },
  methods: {
    logout () {
      this.$auth.logout()
    }
  }
}
</script>
