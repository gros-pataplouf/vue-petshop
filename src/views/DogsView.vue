<template>
    <div class="wrapper">
    <h1>Dogs for adoption</h1>
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
                <tr v-for="dog in dogs" :key="dog.name">
                    <td>{{ dog.name }}</td>
                    <td>{{ dog.breed }}</td>
                    <td>{{ dog.gender }}</td>
                    <td>{{ dog.age }}</td>
                </tr>
            </tbody>
        </template>
    </v-simple-table>
</div>
</template>
<style>
h1 {
    text-align: center;
}
</style>

<script>

import dogs from '@/data/dogs.json'

export default {
  name: 'DogsView',
  data: () => ({
    dogs
    //
  })

}
</script>
