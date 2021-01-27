<template>
  <div class="hello">
   <vue-table
    :tbody-data="Array"
    :headers="Array"
    :custom-options="Object"
    :style-wrap-vue-table="Object"
    :disable-cells="Array"
    :disable-sort-thead="Array"
    :loading="Boolean"
    :parent-scroll-element="Object"
    :select-position="Object"
    :submenu-tbody="Array"
    :submenu-thead="Array"
    v-on:tbody-change-data="changeData"
    v-on:tbody-submenu-click-change-color="changeColorTbody"
    v-on:tbody-submenu-click-change-value="changeValueTbody"
    v-on:thead-submenu-click-change-color="changeColorThead"
    v-on:thead-submenu-click-change-value="changeValueThead"
    v-on:thead-td-sort="sortProduct"></vue-table>
  </div>
</template>

<script>
import VueTable from "vuejs-spreadsheet";

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
  components: {
    VueTable
  }
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
