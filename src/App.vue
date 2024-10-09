<script setup lang="ts">
import Home from './views/Home.vue'
import AOS from 'aos'
import { onMounted } from 'vue'

// importing AOS css style globally
import 'aos/dist/aos.css'

onMounted(() => {
  AOS.init({ once: true })
})
</script>

<template>
  <head>
    <title>Frigid IT Solutions - Expert IT Consulting and Tech Support</title>
    <meta
      name="description"
      content="Frigid IT Solutions offers expert IT consulting, tech support, and cloud services for businesses. Improve your tech infrastructure today."
    />
    <meta
      name="keywords"
      content="IT consulting, tech support, cloud services, IT solutions, business technology"
    />
  </head>

  <Home></Home>
</template>

<style scoped></style>
