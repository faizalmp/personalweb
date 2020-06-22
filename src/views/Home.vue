<template>
  <div class="home">
    <Header/>
    <Profile/>
    <Project/>
  </div>
</template>

<script>
import Header from '../components/Header'
import Profile from '../components/Profile'
import Project from '../components/Project'

export default {
  name: 'Home',
  components: {
    Header,
    Profile,
    Project
  },
  data: () => ({
  })
}
</script>
