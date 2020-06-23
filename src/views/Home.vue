<template>
  <div>
    <Header/>
    <Profile/>
    <Project/>
    <Footer/>
  </div>
</template>

<script>
import Header from '../components/Header'
import Profile from '../components/Profile'
import Project from '../components/Project'
import Footer from '../components/Footer'

export default {
  name: 'Home',
  components: {
    Header,
    Profile,
    Project,
    Footer
  },
  data: () => ({
  })
}
</script>
