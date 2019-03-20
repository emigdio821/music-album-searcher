<template>
  <nav>
    <v-toolbar app dark flat>
      <v-btn
        class="mx-0 hidden-md-and-up"
        icon
        fab
        small
        dark
        @click.stop="drawer = !drawer"
      >
        <v-icon>fas fa-hamburger</v-icon>
      </v-btn>
      <v-toolbar-title class="headline text-uppercase ml-0">
        <span>Album</span>
        <span class="font-weight-light">Searcher</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn flat to="/">Home</v-btn>
        <v-btn flat to="/about">About</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <v-navigation-drawer v-model="drawer" app temporary light>
      <v-list>
        <v-list-tile>
          <v-list-tile-title class="title">
            <span class="text-uppercase">Album</span>
            <span class="font-weight-light text-uppercase">Searcher</span>
          </v-list-tile-title>
        </v-list-tile>
        <v-divider></v-divider>
        <v-list dense class="pt-0">
          <v-list-tile to="/">
            <v-list-tile-action>
              <v-icon>home</v-icon>
            </v-list-tile-action>

            <v-list-tile-content>
              <v-list-tile-title>Home</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>

          <v-list-tile to="/about">
            <v-list-tile-action>
              <v-icon>info</v-icon>
            </v-list-tile-action>

            <v-list-tile-content>
              <v-list-tile-title>About</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list>
        <v-list-tile class="hidden-lg-and-up white--text"> </v-list-tile>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data: () => ({
    drawer: false
  })
};
</script>

<style></style>
