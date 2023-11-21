<script setup>
import Home from './views/Home.vue'
import Tabs from './views/Tabs.vue'
import AboutUs from './views/AboutUs.vue'
import UpcomingEvents from './views/UpcomingEvents.vue'
import PastEvents from './views/PastEvents.vue'
import ContactUs from './views/ContactUs.vue'

</script>

<template>
  <Home/>
  <Tabs />
  <AboutUs />
  <UpcomingEvents />
  <PastEvents />
  <ContactUs />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
