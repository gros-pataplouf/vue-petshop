<template>
  <v-container>
  <v-card>
  <h1>Learn more about your new best friend</h1>
  <template>
  <v-card
    class="mx-auto"
    max-width="500"
    outlined
  >
    <v-list-item three-line>
      <v-list-item-content>
        <div class="text-overline mb-4">
          {{ animal.name }}
        </div>
        <v-list-item-title class="text-h5 mb-1">
          {{ animal.breed }}, {{ animal.age }} years old.
        </v-list-item-title>
        <v-list-item-subtitle> {{ animal.location }} </v-list-item-subtitle>
      </v-list-item-content>

      <v-list-item-avatar
        tile
        size="80"
        color="grey"
      ></v-list-item-avatar>
    </v-list-item>

    <v-card-actions>
      <v-btn
        outlined
        rounded
        text
      >
        Adopt me
      </v-btn>
    </v-card-actions>
  </v-card>
</template>
</v-card>
</v-container>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'PetView',
  data: () => ({
    animal: {}

  }),
  computed: {
    ...mapState(['cats', 'dogs'])
  },
  mounted () {
    this.animal = this[this.$route.params.species][this.$route.params.id]
  }
}
</script>
