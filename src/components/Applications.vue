<template>
  <form name="applications" method="GET">
  <template v-if="true">
      <div class="applications">
        <input type="date" name="date" key="date"/>
        <input type="text" name="position" placeholder="Position" key="position" />
        <input type="text" name="company" placeholder="Company" key="company" />
        <button type="button" name="view_details" v-on:click.left="viewDetails({})">{{ showdetails ? 'Hide Details' : 'View Details' }}</button>
      </div>
  </template>
  <template v-if="showdetails">
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
      <option name="application" value="Application" />
    </select>
     <button
      type="button"
      @click="showInterviewsModal = !showInterviewsModal"
      class="mx-auto w-full flex justify-center rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-base font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-500 sm:mt-0 sm:ml-3 sm:w-auto sm:text-sm">
      Interviews
    </button>
  </template>
  </form>
  <ModalDialog />
</template>

<script>
import ModalDialog from './ModalDialog.vue';

export default {
  data() {
    return {
      showdetails: false,
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
      // Load applications from server
    },
    viewDetails() {
      // Expand application view to show all details OR collapse application view
      // to show fewer details
      this.showdetails = !this.showdetails;
    }
  },
  components: {
   ModalDialog
  }
}
</script>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

select {
  margin-left: 10px;
}
</style>