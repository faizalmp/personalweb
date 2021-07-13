<template>
  <div>
    <section id="project">
      <v-card class="elevation-0" style="border-radius: 0px; min-height: 625px" dark>
        <v-layout column justify-center align-center>
          <v-card-title class="display-2 font-weight-bold text-center">My Works</v-card-title>
          </v-layout>
          <v-container fluid grid-list-xl>
            <v-layout wrap justify-center align-center>
            <v-flex my-4 v-for="item in items" :key="item.title">
              <v-layout justify-center>
                <v-hover v-slot:default="{ hover }">
                  <v-card :elevation="hover ? 4 : 0" style="border-radius: 16px" max-width="300">
                    <v-img :src="item.src" max-width="300">
                      <v-expand-transition>
                        <div v-if="hover"  class="d-flex transition-fast-in-fast-out black v-card--reveal display-3 white--text" style="height: 100%;">
                          <v-layout column>
                            <v-card-title class="title font-weight-bold text-center" style="word-break: normal">{{ item.title }}</v-card-title>
                            <v-card-subtitle>{{ item.subtitle }}</v-card-subtitle>
                            <v-btn class="pb-8" small text :href="item.link" target="_blank"><v-icon left>mdi-link</v-icon>Project Link</v-btn>
                          </v-layout>
                        </div>
                      </v-expand-transition>
                    </v-img>
                  </v-card>
                </v-hover>
              </v-layout>
            </v-flex>
            </v-layout>
          </v-container>
      </v-card>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Project',
  data: () => ({
    items: [
        {
          title: 'Smartland',
          subtitle: 'Smartland is a platform to listing lands.',
          src: 'https://drive.google.com/uc?export=view&id=1suT1UW0vEGoOI43cTimexVJ1e6Xsl9PN',
          link: 'https://smartland.netlify.com/'
        },
        {
          title: 'Piruma Admin',
          subtitle: 'Single web page application to manage room booking.',
          src: 'https://drive.google.com/uc?export=view&id=1na40C0M84QC5SHs4JpygEpDSe5NSlaLL',
          link: 'https://github.com/faizalmp/Piruma-Admin-Website'
        },
        {
          title: 'N202 Innovation Labs Landing Page',
          subtitle: 'Build frontend side of https://n202labs.id',
          src: 'https://drive.google.com/uc?export=view&id=1IFlVg5Av6gFYs81HBtiyaNFf2U-GJic6',
          link: 'https://n202labs.id'
        },
        {
          title: 'Main Bareng REST API',
          subtitle: 'REST API project developed with NodeJS using Adonis. Made for Sanbercode backend development final project',
          src: 'https://drive.google.com/uc?export=view&id=1bCAhGGcoOofauvInvrlhhBHyjdSXX9Zi',
          link: 'https://github.com/faizalmp/main-bareng'
        },
        {
          title: 'Covid Statistic',
          subtitle: 'An app to watch current covid-19 statistic. Made for Riliv recruitmet test. UI by Riliv tech',
          src: 'https://drive.google.com/uc?export=view&id=1g-70kikVocLMV-j6l1OngM-3CJVfN9Oa',
          link: 'https://github.com/faizalmp/CovidStatistic'
        }
    ]
  })
}
</script>

<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .75;
  position: absolute;
  width: 100%;
}
* {
text-transform: none !important;
}
</style>
