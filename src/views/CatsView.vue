<template>
    <div class="wrapper">
    <h1>Cats for adoption</h1>
    <v-data-table
    :headers="Object.keys(cats[0]).map(key => { return { text: key[0].toUpperCase() + key.slice(1), value: key } })"
    :items="cats">
    <template v-slot:[`item.name`]="{ item }">
        <router-link :to="`/pets/cats/${cats.indexOf(item)}`">
          {{ item.name }}
        </router-link>
      </template>
  </v-data-table>
</div>
</template>
<style>
h1 {
    text-align: center;
}
</style>

<script>

// import cats from '@/data/cats'
import { mapState } from 'vuex'

export default {
  name: 'CatsView',
  data: () => ({

  }),
  computed: {
    ...mapState(['cats'])

  }

}
</script>
