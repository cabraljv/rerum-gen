<template>
  <div>
    <!--  <h1>Hello world</h1> -->
    <data-table :rows="rows" :columns="columns" :onClickRow="onClickRow" />
  </div>
</template>

<script>
import DataTable from "./components/DataTable.vue";

export default {
  components: { DataTable },
  name: "App",
  data() {
    return {
      rows: [
        { Field0: 1, Field1: "John Doe", Field2: 30 },
        { Field0: 2, Field1: "Jane Doe", Field2: 25 },
        { Field0: 3, Field1: "Joe Doe", Field2: 20 },
      ],
      columns: ["Field0", "Field1", "Field2"],
    };
  },
  methods: {
    onClickRow(row) {
      console.log("Row clicked", row);
    },
  },
};
</script>

<style></style>
