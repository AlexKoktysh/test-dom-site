<template>
  <v-app>
    <v-main class="app">
      <MainScreen />
    </v-main>
  </v-app>
</template>

<script>
import MainScreen from './components/main-screen.vue'

export default {
  name: 'App',

  components: {
    MainScreen,
  },

  data: () => ({
    //
  }),
}
</script>

<style scoped>
.app {
  display: flex;
  justify-content: center;
}
</style>
