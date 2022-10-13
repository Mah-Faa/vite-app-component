
<template>
  <!-- <Table :fileds="fileds" :items="dataOfTable" />
  <HelloWorld msg="Mahdiyeh + Vue" ok="SAlam" /> -->
  <Map />
</template>



<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
// import HelloWorld from "./components/HelloWorld.vue";
// import Table from "./components/Table.vue";
import Map from "./components/map.vue";

import { ref } from "vue";

const fileds = ref([
  { key: "ID", value: "id" },
  { key: "Name", value: "name" },
  { key: "Family", value: "family" },
  { key: "Sge", value: "age" },
]);
const dataOfTable = ref([
  { id: 1, name: "asqar", family: "oarhadi", age: 32 },
  { id: 4, name: "psqazzzzr", family: "arhadi", age: 62 },
  { id: 2, name: "ali", family: "darhadi", age: 12 },
  { id: 3, name: "nkbar", family: "nase", age: 62 },
]);
</script>



<style scoped>
/* .logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
} */
</style>
