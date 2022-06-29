<template>
  <div>
    <Navbar />
    <Nuxt />
    <Footer />
  </div>
</template>


<script>
import Navbar from "../components/landingComponents/Navbar.vue";
import Footer from "../components/landingComponents/Footer.vue"

export default {
  components: { Navbar, Footer },
};
</script>

<style>
</style>