<template>
  <v-card
    title="Nutrition"
    flat
  >
    <template v-slot:text>
      <v-text-field
        v-model="search"
        label="Search"
        prepend-inner-icon="mdi-magnify"
        variant="outlined"
        hide-details
        single-line
      ></v-text-field>
    </template>

    <v-data-table
      :headers="headers"
      :items="inventory.data"
      :search="search"
    ></v-data-table>
  </v-card>
</template>
<script setup>
  import { ref } from 'vue'
 
  const search = ref('')
    const { data: inventory } = await useFetch('http://localhost:1337/api/inventories');
  const headers = [
    

     
    { key: 'cproduct_name', title: 'Text' },
    { key: 'product_description', title: 'Text' },
    { key: 'quantity', title: 'Number' },
    { key: 'condition', title: 'Text' },
    { key: 'location', title: 'Enumeration' },
    { key: 'acquisition_date', title: 'Enumeration' },
    { key: 'aacquisition_cost', title: 'Date' },
    { key: 'total_cost', title: 'Number' },
    { key: 'remarks', title: 'Number' },

    
  ]

</script> 