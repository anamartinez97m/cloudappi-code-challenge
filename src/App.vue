<template>
  <div id="app">
    <People/>
  </div>
</template>

<script>
import People from './components/People.vue'

export default {
  name: 'App',
  components: {
    People
  }
}
</script>

<style>
  @import './assets/styles/app-styles.css';
</style>
