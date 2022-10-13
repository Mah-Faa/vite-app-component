<template>
  <div class="input-group mb-3">
    <div class="input-group-prepend">
      <span class="input-group-text" id="basic-addon1">?</span>
    </div>
    <input
      type="text"
      notlazy
      class="form-control"
      placeholder="Search"
      aria-label="Search"
      v-model="search"
      aria-describedby="basic-addon1"
    />
  </div>

  <table style="width: 100%" class="table table-hover">
    <thead>
      <tr>
        <th
          v-for="(field, index) in fileds"
          :key="index"
          @click="sortedlistForTable(field.value)"
        >
          {{ field.key }}
          <img style="width: 13px" src="../assets/img/sort.svg" />
        </th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(item, indexj) in items" :key="indexj">
        <td v-for="(field, index) in fileds" :key="index">
          {{ item[field.value] }}
        </td>
      </tr>
    </tbody>
  </table>
</template>
<script setup>
import { ref } from "vue";
import { sortBy } from "lodash";

const search = ref("");
const props = defineProps({
  fileds: Array,
  items: Array,
});
const sort = ref(false);
const sortedList = ref([]);
function sortedlistForTable(col) {
  console.log("col", col);

  sort.value = true;
  sortedList.value = sortBy(props.items, col);
  console.log(sortBy(props.items, col));
}
function filterSearch() {
  console.log(items);
  items.filter((item) => {
    item.toLowerCase().search.toLowerCase();
  });
  const serachInput =computed
}
</script>

<style>
table,
th,
td {
  border: 1px solid rgb(161, 161, 161);
}
</style>
