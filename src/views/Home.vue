<template>
  <div id="home" class="text-white">
    <!-- <Navbar /> -->
    <div class="text-h5 garet eightTrack alignCenter">8 TRACK ENTERTAINMENT</div>
    <div class="details alignCenter kd">
      <p class="text-h5 kd">CURRENT EVENTS</p>
      <p class="text-h3 kd my-8 nowShowing">NOW SHOWING</p>
      <v-btn size="small" density="default" elevation="4" variant="outlined">GET YOUR TICKETS</v-btn>
    </div>
  </div>
</template>
<script setup>
// import Navbar from '../components/Navbar.vue';

</script>

<style scoped>

#home {
  position: relative;
  background-image: url('../assets/Home.jpg');
  background-size: cover;
  background-position: bottom, center;
  height: 100vh;
  width: 100vw;
}

.alignCenter {
  position:absolute;
  display:block;
  left:0;
  right:0;
  margin:auto;
  z-index: 99;
}

.eightTrack {
  letter-spacing: 10px !important;
  top: 10%;
}

.details {
  top: 40%;
}

@media only screen and (max-width: 768px) {

  .alignCenter {
    position:absolute;
    display:block;
    left:0;
    right:0;
    width: 40%;
    top: 50%;
    margin:auto;
    z-index: 99;
  }

  .eightTrack {
    display: flex;
    justify-content: center;
    letter-spacing: 5px !important;
    top: 5%;
  }

  .details {
    top: 30%;
  }

  .nowShowing {
    display:flex;
    justify-content: center;
  }
}
</style>
