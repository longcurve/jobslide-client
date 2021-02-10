<template>
    <div class="should-have-a-children scroll-me overflow:auto">
      <div class="applications">
        <input type="date" name="date" />
        <input type="text" name="position" placeholder="Position" />
        <input type="text" name="company" placeholder="Company" />
        <button name="view_details" v-on:click.left="ViewDetails({})">View Details</button>
        <router-link to="/application-details" tag="button">Application Details</router-link>
      </div>
    </div>
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