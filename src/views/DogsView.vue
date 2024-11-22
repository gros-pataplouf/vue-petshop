<template>
    <div class="wrapper">
    <h1>Dogs for adoption</h1>
    <v-data-table
    :headers="Object.keys(dogs[0]).map(key => { return { text: key[0].toUpperCase() + key.slice(1), value: key } })"
    :items="dogs">
      <template v-slot:[`item.name`]="{ item }" >
        <router-link :to="`/pets/dogs/${dogs.indexOf(item)}`">
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
import { mapState } from 'vuex'

export default {
  name: 'DogsView',
  data: () => ({
  }),
  computed: {
    ...mapState(['dogs'])
  }

}
</script>
