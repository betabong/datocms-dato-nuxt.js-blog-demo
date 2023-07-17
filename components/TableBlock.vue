<script setup lang="ts">
const props = defineProps<{
  table: {
    data: Record<string, string>[]
    columns: string[]
  }
  id: string
}>()
</script>

<template>
  <div class="table-responsive">
    <table class="table table-striped">
      <thead>
        <tr>
          <th v-for="column in props.table.columns" :key="column">
            {{ column }}
          </th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="row in props.table.data" :key="row.id">
          <td v-for="column in props.table.columns" :key="column">
            {{ row[column] }}
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>
