<template>
  <div class="applications">
    <input type="date" name="date" />
    <input type="text" name="position" placeholder="Position" />
    <input type="text" name="company" placeholder="Company" />
    <input type="text" name="location" placeholder="City, ST" />
    <input type="text" name="contact_first_name" placeholder="John" />
    <input type="text" name="contact_last_name" placeholder="Doe" />
    <input type="text" name="contact_phone" placeholder="xxx-xxx-xxxx" />
    <select name="application_status">
      <option name="applied" value="Applied" />
      <option name="notapplied" value="Not Applied" />
    </select>
  </div>
</template>

<script>

export default {
  data() {
    return {

    };
  },
  methods: {
    save() {
      // Save all applications to the server
    },
    saveLocally() {
      // Save to local storage
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
