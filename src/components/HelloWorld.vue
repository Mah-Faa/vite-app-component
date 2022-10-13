<template>
  <!-- <Table /> -->

  <div class="card">
    <button type="button" @click="count++">count is {{ count }}</button>
    <br />
    helllo i am asqar: {{ asqar }}
  </div>
</template>

<script setup>
import { ref } from "vue";
// import Table from "./Table.vue";

defineProps({
  msg: String,
  ok: String,
});

const count = ref(0);
const asqar = ref(2546);
</script>



<style scoped>
.read-the-docs {
  color: #888;
}
</style>
