<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
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
  <Home></Home>
</template>

<style scoped></style>
