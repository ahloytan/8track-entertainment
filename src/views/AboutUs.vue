<template>
  <div id="aboutUs" class="py-14 text-white">
    <p class="text-h4 pb-10">About Us</p> <!-- text-xl-h2 -->
    <p class="text-h6 py-4">A dedicated team of <span class="font-italic highlight">Event Enthusiasts</span></p> <!-- text-xl-h4 -->
    <p class="text-h6 py-4">Transforming ideas into unforgettable experiences</p>
    <p class="text-h6 py-4">Sharing moments that go beyond the <span class="font-italic highlight">Ordinary</span>.</p>
    <div class="d-flex justify-center align-center mt-4">
      <v-btn density="default" rounded="xl" elevation="4" variant="outlined">Private</v-btn>
      <v-btn density="default" rounded="xl" elevation="4" class="mx-4 mx-md-8 mx-lg-32" variant="outlined">Corporate</v-btn>
      <v-btn density="default" rounded="xl" elevation="4" variant="outlined">Public</v-btn>
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
  font-family: "KudryashevDisplay" !important;
}

.highlight {
  color: #FF914D;
}
</style>
