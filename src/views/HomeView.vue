<!-- Start/bokningssida -->
<script setup>
// Hämtning av komponenter
import Hero from "../components/Hero.vue"
import Booking from "../components/Booking.vue"

import { ref } from 'vue'
const hide = ref(true)
</script>

<template>
  <Hero />
  <h1 class="hero-text">Kaffe-Baren</h1>
  <button type="button" class="btn btn-lg btn-secondary" @click="hide = !hide">Boka din kaffe</button>
  <div v-if="!hide">
    <Booking />
</div>
</template>


<style scoped>
.hero-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: black;
}

.btn {
  position: absolute;
  top: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: gray;
}
</style>
