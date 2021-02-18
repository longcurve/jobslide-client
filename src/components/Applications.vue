<template>
  <template v-if="show-brief">
      <div class="applications">
        <input type="date" name="date" key="date"/>
        <input type="text" name="position" placeholder="Position" key="position" />
        <input type="text" name="company" placeholder="Company" key="company" />
        <button name="view_details" v-on:click.left="ViewDetails({})">View Details</button>
      </div>
  </template>
  <template v-else-if="show-details">
    <br /><input type="text" name="location" placeholder="City, ST" />
    <input type="text" name="contact_first_name" placeholder="John" />
    <input type="text" name="contact_last_name" placeholder="Doe" /><br />
    <input type="text" name="contact_phone" placeholder="xxx-xxx-xxxx" />
    <select name="application_status">
      <option name="applied" value="Applied" />
      <option name="notapplied" value="Not Applied" />
    </select>
     <select name="application_method">
      <option name="resume" value="Resume" />
      <option name="application" value="Application" /><br />
      
    </select>
  </template>
</template>

<script>

export default {
  data() {
    return {
     applications: this.loadApplications()
    };
  },
  methods: {
    save() {
      // Save all applications to the server
    },
    saveLocally() {
      // Save to local storage
    },
    loadApplications() {

    },
    ViewDetails() {
      this.currentView = "Application-Details";
    }
  },
  components: {
   
  }
}
</script>