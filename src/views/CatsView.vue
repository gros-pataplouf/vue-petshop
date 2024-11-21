<template>
    <div class="wrapper">
    <h1>Cats for adoption</h1>
    <v-data-table :headers="headers" :items="cats"></v-data-table>

</div>
</template>
<style>
h1 {
    text-align: center;
}
</style>

<script>

import cats from '@/data/cats'

export default {
  name: 'CatsView',
  data: () => ({
    headers: Object.keys(cats[0]).map(key => { return { text: key[0].toUpperCase() + key.slice(1), value: key } }),
    cats

  })

}
</script>
