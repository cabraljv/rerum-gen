<template>
  <div>
    <h1>Hello world</h1>
    <data-table :rows="rows" :columns="columns" />
  </div>
</template>

<script>
import DataTable from './components/DataTable.vue'

export default {
  components: { DataTable },
  name: 'App',
  data() {
    return {
      rows: [
        { id: 1, name: 'John Doe', age: 30 },
        { id: 2, name: 'Jane Doe', age: 25 },
        { id: 3, name: 'Joe Doe', age: 20 }
      ],
      columns: ['id','name', 'age']
    }
  }
}
</script>

<style>

</style>