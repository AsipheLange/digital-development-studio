<script setup>
import Navbar from './components/layout/Navbar.vue'
import Footer from './components/layout/Footer.vue'
</script>

<template>
  <div class="min-h-screen bg-[#F8F9FB] text-[#111827]">
    <Navbar />

    <RouterView />

    <Footer />
  </div>
</template>