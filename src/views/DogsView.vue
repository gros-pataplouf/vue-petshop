<template>
    <div class="wrapper">
    <h1>Dogs for adoption</h1>
    <v-data-table :headers="headers" :items="dogs"></v-data-table>

</div>
</template>
<style>
h1 {
    text-align: center;
}
</style>

<script>

import dogs from '@/data/dogs'

export default {
  name: 'DogsView',
  data: () => ({
    headers: Object.keys(dogs[0]).map(key => { return { text: key[0].toUpperCase() + key.slice(1), value: key } }),
    dogs

  })

}
</script>
