<template>
  <!-- This just loads spreadsheet into the app, the surrounding stuff will be in HTML template -->
  <Applications />
</template>

<script>
import Applications from './components/Applications.vue'

export default {
  name: 'App',
  components: {
    Applications
  }
}
</script>