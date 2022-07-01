<template>
  <div>
    <navbar/>
    <Hero />
    <Testimonials />
    <Features />
    <CTA />
    
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Navbar from '../components/landingComponents/Navbar.vue'
import Hero from '../components/landingComponents/Hero.vue'
import Features from '../components/landingComponents/Features.vue'
import CTA from '../components/landingComponents/CTA.vue'
import Testimonials from '../components/landingComponents/Testimonials.vue'
import Topbar from '../components/topbarComponents/Topbar.vue'



export default Vue.extend({
  components: { Navbar, Hero, Features, CTA, Testimonials, Topbar },
  name: 'IndexPage',

})
</script>

<style>
</style>