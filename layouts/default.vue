<template>
  <div>
      <Navbar />    
      <b-container>
        <Nuxt />
      </b-container>
      <Footer />
  </div>
</template>

<script>
import Navbar from '../components/Navbar'
import Footer from '../components/Footer'

export default {
  components: {
    Navbar,
    Footer
  },
  data: () => {
    return {

    }
  }
}
</script>

<style lang="scss">
@import '../assets/scss/custom.scss'
</style>
