<template>
  <v-app id="app">
    <header>
    <v-app-bar tag="nav" class="navbar">
      <router-link to="/"><v-btn active-color="white" text>Home</v-btn></router-link>
      <router-link to="/cats"><v-btn text>Cats</v-btn></router-link>
      <router-link to="/dogs"><v-btn text>Dogs</v-btn></router-link>
    </v-app-bar>
  </header>
  <v-container grid-list-xs>
    <router-view/>
  </v-container>
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

.v-toolbar__content {
    width: 100vw;
    background-color: #f08080;
    display: flex;
    justify-content: space-evenly;
}

.navbar {

  a {
    font-weight: bold;
    color: #33388a;
    &>span>a, &>span {
      display: block;
      padding: auto;
    }

    &.router-link-exact-active>button>span {
      color: whitesmoke;
    }
  }
}
</style>
