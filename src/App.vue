<template>
  <!-- This just loads spreadsheet into the app, the surrounding stuff will be in HTML template -->
  <Spreadsheet />
</template>

<script>
import Spreadsheet from './components/Spreadsheet.vue'

export default {
  name: 'App',
  components: {
    Spreadsheet
  }
}
</script>