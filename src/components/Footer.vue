<template>
  <v-footer dark>
    <v-card class="flex transparent" flat tile>
      <v-layout justify-center column>
      <v-card-text class="text-center">
        <strong class="subheading font-weight-bold">Contact me</strong><br>
        <v-card-text class="text-center">
          <v-btn v-for="item in contacts" :key="item.icon" class="mx-2 text-center" :href="item.link" target="_blank" icon>
            <v-icon size="24px">{{ item.icon }}</v-icon>
          </v-btn>
        </v-card-text>
      </v-card-text>
      <v-card-text class="py-2 white--text font-weight-thin text-center">
        &copy;{{ new Date().getFullYear() }} <strong>Faizal Muhammad Priyowibowo</strong>
      </v-card-text>
      </v-layout>
    </v-card>
  </v-footer>
</template>

<script>
  export default {
    name: 'Footer',
    data: () => ({
      contacts: [
        { icon:'mdi-email', link: 'mailto:faizalpriyowibowo@gmail.com' },
        { icon:'mdi-linkedin', link: 'https://linkedin.com/in/faizalmp' },
        { icon:'mdi-github', link: 'https://github.com/faizalmp' },
        { icon:'mdi-instagram', link: 'https://instagram.com/faizalempe' },
      ]
    })
  }
</script>