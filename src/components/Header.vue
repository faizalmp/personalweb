<template>
  <div id="header">
    <v-card class="elevation-0" style="border-radius: 0px; min-height: 625px" :color="$store.state.palette.primary" dark>
      <v-layout align-center column justify-center>
          <v-flex mt-12>
            <v-layout class="hidden-md-and-down" align-center justify-center>
              <v-img src="../assets/header_character.png" max-height="250" max-width="250"></v-img>
            </v-layout>
            <v-layout class="hidden-lg-and-up" align-center justify-center>
              <v-img src="../assets/header_character.png" max-height="200" max-width="200"></v-img>
            </v-layout>
          </v-flex>
          <v-flex pb-16 mt-8>
            <p class="text-center">
              <vue-typed-js class="hidden-lg-and-up" :strings="title">
              <span class="typing headline font-weight-bold"></span>
              </vue-typed-js>
              <vue-typed-js class="hidden-md-and-down" :strings="title">
              <span class="typing display-2 font-weight-bold"></span>
              </vue-typed-js>
            </p>
          </v-flex>
      </v-layout>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data: () => ({
    title: ['Hi !', 'I am Faizal Muhammad Priyowibowo', 'Nice to meet you', 'Welcome to my site :)']
  })
}
</script>