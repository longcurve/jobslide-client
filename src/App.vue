<template>

  <!-- The top template of the entire web application. Here is where we build the website
  overall website design. Embedding Applications List (Applications.vue) and any other
  application areas as website content. -->
  <Applications />
</template>

<style>
input[type="text"] {
  margin: 5px;
}
</style>

<script>
import Applications from './components/Applications.vue'

export default {
  name: 'App',
  components: {
    Applications
  }
}
</script>