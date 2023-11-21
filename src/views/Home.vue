<template>
  <div id="home">
    <Navbar />
    <img class="alignCenter" src="../assets/logo.png"> 
  </div>
</template>
<script setup>
import Navbar from '../components/Navbar.vue';

</script>

<style scoped>

#home {
  position: relative;
  background-image: url('../assets/Home1.png');
  background-size: cover;
  background-position: center, center;
  height: 100vh;
  width: 100vw;
}

.alignCenter {
  position:absolute;
  display:block;
  left:0;
  right:0;
  bottom: 50%;
  margin:auto;
  z-index: 99;
}

@media only screen and (max-width: 768px) {
  .alignCenter {
    position:absolute;
    display:block;
    left:0;
    right:0;
    width: 90%;
    top: 25%;
    margin:auto;
    z-index: 99;
  }
}
</style>
