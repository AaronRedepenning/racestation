<template>
  <v-app id="racestation">
    <v-navigation-drawer :clipped="$vuetify.breakpoint.lgAndUp" v-model="drawer" fixed app>
      <v-list dense>
        <template v-for="item in items">
          <v-list-tile :key="item.text">
            <v-list-tile-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>
                {{ item.text }}
              </v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </template>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar :clipped-left="$vuetify.breakpoint.lgAndUp" color="light-blue" dark app fixed>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <v-toolbar-title>Racestation</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn icon>
          <v-icon>search</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>view_module</v-icon>
        </v-btn>
      </v-toolbar>
    <v-content>
      <v-container fluid fill-height>
        <v-layout justify-center align-center>
          <!-- Page Content -->
          <router-view></router-view>
        </v-layout>
      </v-container>
    </v-content>
    <v-footer class="pa-3">
      <v-spacer></v-spacer>
      <div>&copy; {{ new Date().getFullYear() }}</div>
  </v-footer>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      drawer: null,
      items: [
        { icon: 'cloud', text: 'Weather' }
      ]
    })
  }
</script>