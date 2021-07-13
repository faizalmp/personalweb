<template>
  <div>
    <section id="involved-project">
      <v-card class="elevation-0" style="border-radius: 0px; min-height: 625px" dark>
        <v-layout column justify-center align-center>
          <v-card-title class="display-2 font-weight-bold text-center">Involved Project</v-card-title>
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
                            <v-btn v-if="item.link" class="pb-8" small text :href="item.link" target="_blank"><v-icon left>mdi-link</v-icon>Project Link</v-btn>
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
          src: 'https://drive.google.com/uc?export=view&id=1GVo4Lrigs5lF5nhfVM8RIgWfSjnodpwZ',
          link: 'https://drive.google.com/folderview?id=1zk-00Zx4zBgTvAUBMXP3aNjPXIMJmXyS'
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
        },
        {
          title: 'MeetingYuk',
          subtitle: 'MeetingYuk is an app to book room or place for meeting.',
          src: 'https://play-lh.googleusercontent.com/BSdg0BXxFEQjKEROA5FBlAH4hQf2VwGCO9xSmQ78_Sn39XYnFZhOn11gTJ8Lu8bI4eqb=s180-rw',
          link: 'https://play.google.com/store/apps/details?id=id.n202.meetingyuk'
        },
        {
          title: 'MerchantYuk',
          subtitle: 'MerchantYuk is a merchant-side app for MeetingYuk.',
          src: 'https://play-lh.googleusercontent.com/_EU6YEWbID1tTzik5lUehKrIN5r_CPxugkIKx9XUZnkCVW4mSxiY3ihp4m5tiehyLw=s180-rw',
          link: 'https://play.google.com/store/apps/details?id=id.n202.merchantyuk'
        },
        {
          title: 'Teman Kajian',
          subtitle: 'Teman Kajian is an android app for search moslem lecture.',
          src: 'https://drive.google.com/uc?export=view&id=1XINMoOSY2HWPDyMN-oxQF1dYx8hHMF1l',
          link: 'https://play.google.com/store/apps/details?id=id.ardifact.temanhijrah'
        },
        {
          title: 'Kios Sehat',
          subtitle: 'An app to watch current Kios Sehat user status. Made by Widya Imersif Teknologi.',
          src: 'https://play-lh.googleusercontent.com/8GJTh9ndGXVxR476zW-TzULsW25t-owZWfsfbS9cSz92CUrmOv4tl6-M-woHnbCEJ9s=s180-rw',
          link: 'https://play.google.com/store/apps/details?id=iot.widya.kiossehatuser'
        },
        {
          title: 'Kios Sehat (Device App)',
          subtitle: 'An app for kios sehat device for control self-medical check-up. Made by Widya Imersif Teknologi.',
          src: 'https://drive.google.com/uc?export=view&id=1C-TWmqB0Okt-kKQLX5ECvjLnv3Rlvm46'
        },
        {
          title: 'Matador Tracker',
          subtitle: 'An android app to set tracker device and watch the device state. Made by Widya Imersif Teknologi.',
          src: 'https://drive.google.com/uc?export=view&id=1MO2xrOr8-h1l_pQN4USfFzKXLp3ncCDv'
        },
        {
          title: 'SSG',
          subtitle: 'An android app to video conference, scheduling, and set smart safety glasses. Made by Widya Imersif Teknologi.',
          src: 'https://drive.google.com/uc?export=view&id=1_jzdfZOza1XrjN-eloysZvkFhfMcEmEX'
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
