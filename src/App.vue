<script setup>
import Hero from "./components/Hero.vue"
import ClientLogos from './components/ClientLogos.vue'
import Features from './components/Features.vue'
import Discover from './components/Discover.vue';
import Tabs from './components/Tabs.vue';
import NavBar from "./components/NavBar.vue"
import LaunchPhone from "./components/LaunchPhone.vue"
import CreateAccount from "./components/CreateAccount.vue"
import Testimonials from "./components/Testimonials.vue"
import ImageGallery from "./components/ImageGallery.vue"
import Pricing from "./components/Pricing.vue"
import FAQ from "./components/FAQ.vue"
import CallToAction from "./components/CallToAction.vue"
import ContactInfo from "./components/ContactInfo.vue"
import Footer from "./components/Footer.vue"
</script>

<template>

  <div data-spy="scroll" data-target="#navbar" data-offset="30">
      <!-- Nav Menu -->
      <NavBar/>
      <Hero/>
      <ClientLogos/>
      <Features/>
      <Discover/>
      <Tabs/>
      <LaunchPhone/>
      <CreateAccount/>
      <Testimonials/>
      <ImageGallery/>
      <Pricing/>
      <FAQ/>
      <CallToAction/>
      <ContactInfo/>     
      <Footer/>     

  </div>
</template>

<style scoped>

</style>
