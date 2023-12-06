<template>
<table class="table">
  <thead>
    <tr>
      <th v-for="column in columns" :key="column">{{ column }}</th>
    </tr>
  </thead>
  <tbody>
    <tr v-for="row in rows" :key="row.id">
      <td v-for="column in columns" :key="column">{{ row[column] }}</td>
    </tr>
  </tbody>
</table>
  
</template>

<script>
export default {
  name: 'DataTable',
  props: ['rows', 'columns']
}
</script>

<style>

</style>