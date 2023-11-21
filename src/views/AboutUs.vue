<template>
  <div id="aboutUs" class="py-14 text-white">
    <p class="text-h4 text-md-h2 pb-10">About Us</p>
    <p class="text-h6 text-md-h4 py-4">A dedicated team of <span class="font-italic highlight">Event Enthusiasts</span></p>
    <p class="text-h6 text-md-h4 py-4">Transforming ideas into unforgettable experiences</p>
    <p class="text-h6 text-md-h4 py-4">Sharing moments that go beyond the <span class="font-italic highlight">Ordinary</span>.</p>
    <div class="d-flex justify-center align-center mt-4">
      <v-btn density="default" rounded="xl" elevation="4" variant="outlined">Private</v-btn>
      <v-btn density="default" rounded="xl" elevation="4" class="mx-4 mx-md-8 mx-lg-32">Corporate</v-btn>
      <!-- <v-btn density="default" rounded="xl" elevation="4" variant="plain">Public</v-btn> -->
      <a href="" class="text-decoration-underline text-white text-h6">Public</a>
    </div>
  </div>
</template>
<script setup>

</script>

<style scoped>
#aboutUs {
  background-color: #1C1919;
}

p, btn, a {
  font-family: "Kudryashev Display Sans" !important;
}

.highlight {
  color: #FF914D;
}
</style>
