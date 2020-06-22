<template>
  <div id="project">
    <v-card class="elevation-0">
      <v-layout column justify-center align-center>
        <v-card-title class="display-2 font-weight-bold text-center">My Works</v-card-title>
        </v-layout>
        <v-list class="mx-2">
          <v-list-item v-for="item in items" :key="item.title" style="border-radius: 16px">
              <v-card elevation="0" class="ma-4">
                <v-layout row>
                  <v-img style="border-radius: 16px" src="https://cdn.vuetifyjs.com/images/cards/mountain.jpg" max-width="300"></v-img>
                  <v-flex style="max-width:75%">
                  <v-layout column>
                      <v-card-title class="display-1 font-weight-bold">{{ item.title }}</v-card-title>
                      <v-card-subtitle>{{ item.subtitle }}</v-card-subtitle>
                  </v-layout>
                  </v-flex>
                </v-layout>
              </v-card>
          </v-list-item>
        </v-list>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'Project',
  data: () => ({
    items: [
        { title: 'Kupuku', subtitle: 'Kupukuasdsabdhasdjaskdjasdasnjkdkajsndasjdasndasjdnaksdsnakasdbsasjkdnsakdjansdkjasndkjasdkjasndjknasjkdnkasndsajkdajdskasndasahdbsahdbashdasbdhsbadhasbdhasbdhasbdhasbhdsabhdbashdbashdbashdasbdashbdhsa', src: '' }
    ]
  })
}
</script>