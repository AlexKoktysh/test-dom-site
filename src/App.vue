<template>
  <v-app class="app">
    <v-main>
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
}
</script>

<style scoped lang="scss">
.app {
  display: flex;
  justify-content: center;
}
</style>
