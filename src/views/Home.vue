<template>
  <div>
    <Header/>
    <Profile/>
    <Project/>
    <Involved/>
    <Footer/>
  </div>
</template>

<script>
import Header from '../components/Header'
import Profile from '../components/Profile'
import Project from '../components/Project'
import Involved from '../components/InvolvedProject'
import Footer from '../components/Footer'

export default {
  name: 'Home',
  components: {
    Header,
    Profile,
    Project,
    Involved,
    Footer
  },
  data: () => ({
  })
}
</script>
