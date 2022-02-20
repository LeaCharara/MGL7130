<template>
<v-app>
  <div id="app">
    <router-view />
    <!-- <NavBar /> -->
  </div>
</v-app>
</template>
<script>
// import NavBar from './components/NavBar.vue'
export default {
	name: 'App',
  components: {
    // NavBar
  }
};
</script>
<style>
  * {
    font-family : "system-ui"
  }
</style>