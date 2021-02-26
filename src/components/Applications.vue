<template>
  <template v-if="true">
      <div class="applications">
        <input type="date" name="date" key="date"/>
        <input type="text" name="position" placeholder="Position" key="position" />
        <input type="text" name="company" placeholder="Company" key="company" />
        <button name="view_details" v-on:click.left="viewDetails({})">{{ showdetails ? 'Hide Details' : 'View Details' }}</button>
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
    </select><br />

  </template>
  <template>
    <teleport to="body">
    <div
        class="w-1/2 bg-white rounded-lg text-left overflow-hidden shadow-xl"
        role="dialog"
        ref="modal"
        aria-modal="true"
        aria-labelledby="modal-headline"
    >
       Awiwi
    </div>
  </teleport>
</template>
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

    },
    viewDetails() {
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
</style>