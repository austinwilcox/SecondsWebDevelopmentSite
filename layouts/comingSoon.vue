<template>
  <div>
    <Navbar />
    <b-container>
       <b-row>
         <b-col>
          <h1>Coming Soon</h1>  
         </b-col>
      </b-row> 
    </b-container>
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
import NavBar from '../components/Navbar'
import Footer from '../components/Footer'

export default {
  components: {
    NavBar,
    Footer
  } 
}
</script>

<style>
body {
  font-size: 18px;
  font-family: Georgia, 'Times New Roman', Times, serif;
  background-color: #ffffff;
}
</style>
