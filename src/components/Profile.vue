<template>
  <div>
    <section id="profile">
      <v-card :color="$store.state.palette.secondary" elevation="0" style="border-radius: 0px; min-height: 625px">
        <v-layout align-center justify-center column>
          <v-card-title class="display-2 text-center font-weight-bold">about me</v-card-title>
          <v-flex align-self-center>
            <v-layout class="hidden-md-and-down" align-center justify-center>
              <v-img src="../assets/profile_photo.png" max-height="300" max-width="300"></v-img>
            </v-layout>
            <v-layout class="hidden-lg-and-up" align-center justify-center>
              <v-img src="../assets/profile_photo.png" max-height="200" max-width="200"></v-img>
            </v-layout>
            <v-layout class="my-4 px-8" column align-center justify-center>
              <p class="body-1 text-center">
                <span class="font-weight-bold">I am Faizal Muhammad Priyowibowo,</span><br>
                <span>I am a person who interest in mobile development and front-end development especially with Java, Kotlin, and VueJS. I am always willing to learn and improve my works. Computer is my friend, especially code. I love design, but my design makes me haha.</span>
              </p>
              <v-card-text class="text-center">
                <v-btn v-for="item in contacts" :key="item.icon" class="mx-2 text-center" :href="item.link" target="_blank" icon>
                  <v-icon size="24px">{{ item.icon }}</v-icon>
                </v-btn>
              </v-card-text>
              <v-btn rounded outlined href="https://drive.google.com/file/d/1j2UbtB3MRhci4U3lHpB4LmsIDOfyGBgR/view?usp=sharing" target="_blank">See my resume</v-btn>
           </v-layout>
          </v-flex>
      </v-layout>
      </v-card>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Profile',
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