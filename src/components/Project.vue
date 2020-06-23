<template>
  <div>
    <section id="project">
      <v-card class="elevation-0" style="border-radius: 0px; min-height: 625px" dark>
        <v-layout column justify-center align-center>
          <v-card-title class="display-2 font-weight-bold text-center">My Works</v-card-title>
          </v-layout>
          <v-container fluid grid-list-xl>
            <v-layout wrap justify-center align-center>
            <v-flex mt-8 v-for="item in items" :key="item.title">
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
          title: 'Kupuku',
          subtitle: 'Kupuku is an educational AR game to study butterflies more fun.',
          src: 'https://drive.google.com/uc?export=view&id=1LT0_DrFLr2PVXfhotbbOO8cNzpb6cCpc',
          link: 'https://drive.google.com/folderview?id=1zk-00Zx4zBgTvAUBMXP3aNjPXIMJmXyS'
        },
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
          title: 'Jengukin',
          subtitle: 'Jengukin is an android app to help patient and family keep connected.',
          src: 'https://drive.google.com/uc?export=view&id=1kFTSN-1ipzsQX89VwQkIcklAghebJ-jv',
          link: 'https://github.com/faizalmp/Kumpulan-Proyek-Kuliah-Kelompok/tree/master'
        },
        {
          title: 'TAYO',
          subtitle: 'TAYO is an android app to track the nearest bus get bus stop informations, bus tracks, and bus schedules.',
          src: 'https://drive.google.com/uc?export=view&id=1bhM96ZikWUsi8IhmGoOTxKdk833JQvBL',
          link: 'https://github.com/faizalmp/Kumpulan-Proyek-Kuliah-Kelompok/tree/master'
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
