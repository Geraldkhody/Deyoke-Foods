<template>
  <Navbar />
  <Home />
  <About />
  <Product />
  <Testimonial />
  <Team /> 
  <FAQ />
  <Footer />
</template>

<script setup>
import Home from "@/Screen/Home/Home.vue"
import About from "@/Screen/About/About.vue"
import Navbar from "@/Screen/Home/Navbar.vue"
import Product from "@/Screen/Products/Products.vue"
import Testimonial from "@/Screen/Testimonials/Testimonials.vue"
import Team from "@/Screen/Team/Team.vue"
import FAQ from "@/Screen/FAQ/FAQ.vue"
import Footer from "@/Screen/Footer/Footer.vue"


</script>


<style>
:root {
  --primary-color: #014751;
  --light-green: #9FE82B;
  --dark-green: #083F3D;
  --text-green: #445D65;
  --navbar-height: 4.5rem;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family:  sans-serif;
}

html {
  scroll-behavior: smooth;
}

#app {
  margin: auto;
  transition: 0.3s linear;
}
</style>
