<template>
  <div>
    <v-app-bar v-if="scrollPosition < 625" app tile clipped-left flat :color="$store.state.palette.primary" dark>
      <v-app-bar-nav-icon class="hidden-lg-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="align-center center justify-center">
        <v-btn class="elevation-0" to="/" color="transparent" @click="$vuetify.goTo('#header')">
          <v-img max-width="128" src="../assets/logo/logo_white.png"></v-img>
        </v-btn>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-layout class="hidden-sm-and-down" justify-end>
        <v-btn class="text-lowercase subtitle-1 font-weight-bold" small text v-for="item in items" :key="item.title" @click="$vuetify.goTo(item.link)">{{ item.title }}</v-btn>
      </v-layout>
    </v-app-bar>
    <v-app-bar v-if="scrollPosition >= 625 && scrollPosition < 1250" app tile clipped-left flat :color="$store.state.palette.secondary">
      <v-app-bar-nav-icon class="hidden-lg-and-up" @click.stop="drawer = !drawer" style="color: #0D6064"></v-app-bar-nav-icon>
      <v-toolbar-title class="align-center center justify-center">
        <v-btn class="elevation-0" to="/" color="transparent" @click="$vuetify.goTo('#header')">
          <v-img max-width="128" src="../assets/logo/logo_tosca.png"></v-img>
        </v-btn>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-layout class="hidden-sm-and-down" justify-end>
        <v-btn class="text-lowercase subtitle-1 font-weight-bold" :color="$store.state.palette.primary" small text v-for="item in items" :key="item.title" @click="$vuetify.goTo(item.link)">{{ item.title }}</v-btn>
      </v-layout>
    </v-app-bar>
    <v-app-bar v-if="scrollPosition >= 1250" app tile clipped-left flat color="grey darken-4" dark>
      <v-app-bar-nav-icon class="hidden-lg-and-up" @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="align-center center justify-center">
        <v-btn class="elevation-0" to="/" color="transparent" @click="$vuetify.goTo('#header')">
          <v-img max-width="128" src="../assets/logo/logo_white.png"></v-img>
        </v-btn>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-layout class="hidden-sm-and-down" justify-end>
        <v-btn class="text-lowercase subtitle-1 font-weight-bold" small text v-for="item in items" :key="item.title" @click="$vuetify.goTo(item.link)">{{ item.title }}</v-btn>
      </v-layout>
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" app temporary dark :color="$store.state.palette.primary">
      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" @click="$vuetify.goTo(item.link); drawer = false">
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data: () => ({
    drawer: null,
    items: [
      { title: 'about me', link: '#profile' },
      { title: 'my works', link: '#project' }
    ],
    scrollPosition: null
  }),
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY
    }
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll)
  }
}
</script>

<style>
.v-btn:before {
  display: none;
}
</style>
