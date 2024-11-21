<template>
  <v-app id="app">
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/cats">Cats</router-link> |
      <router-link to="/dogs">Dogs</router-link>
    </nav>
    <router-view/>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    //
  })
}
</script>

<style>

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #33388a;

    &.router-link-exact-active {
      color: #c2346a;
    }
  }
}
</style>
