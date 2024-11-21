<template>
    <div>
        <h1>Cats for adoption</h1>
        <template>
            <v-simple-table>
                <template v-slot:default>
                    <thead>
                        <tr>
                            <th class="text-left">
                                Name
                            </th>
                            <th class="text-left">
                                Breed
                            </th>
                            <th class="text-left">
                                Gender
                            </th>
                            <th class="text-left">
                                Age
                            </th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="cat in cats" :key="cat.name">
                            <td>{{ cat.name }}</td>
                            <td>{{ cat.breed }}</td>
                            <td>{{ cat.gender }}</td>
                            <td>{{ cat.age }}</td>
                        </tr>
                    </tbody>
                </template>
            </v-simple-table>
        </template>
    </div>
</template>

<style>
h1 {
    text-align: center;
}
</style>
<script>

import cats from '@/data/cats.json'

export default {
  name: 'CatsView',
  data: () => ({
    cats
    //
  })

}
</script>
