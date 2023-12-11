<template>
  <div class="container text-center">
    <div class="table-responsive">
      <table
        class="table table-light table-striped table-hover table-bordered table-sm align-middle caption-top"
      >
        <thead class="table-primary">
          <tr>
            <th></th>
            <th v-for="column in columns" :key="column">{{ column }}</th>
          </tr>
        </thead>
        <tbody class="table-group-divider">
          <tr v-for="row in rows" :key="row.id" @click="onClickRow(row)">
            <div>
              <input
                class="form-check-input"
                type="checkbox"
                id="checkboxNoLabel"
                value=""
                aria-label="..."
              />
            </div>
            <td v-for="column in columns" :key="column">{{ row[column] }}</td>
          </tr>
        </tbody>
        <caption class="text-left">
          DataTable
        </caption>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "DataTable",
  props: ["rows", "columns", "onClickRow"],
};
</script>

<style></style>
