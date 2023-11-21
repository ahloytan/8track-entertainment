<template>
  <v-container fluid id="upcomingEvents">
    <div id="textHolder" class="alignCenter">
      <img :src="imgSource">
    </div>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
    }
  },
  computed: {
    imgSource() {
      let image = 'uE1';
      if (window.innerWidth <= 420) image = 'uE2';
      return new URL(`../assets/${image}.png`, import.meta.url).href
    }
  }
}
</script>
<style scoped>
#upcomingEvents {
  position: relative;
  background-image: url('../assets/upcomingEvents.png');
  background-size: cover;
  background-position: center;
  height: 100vh;
  font-family: "Metropolis";
}

.alignCenter {
  position:absolute;
  display:block;
  left:0;
  right:0;
  top: 25%;
  margin:auto;
  z-index: 99;
}

@media only screen and (max-width: 768px) {

}
</style>
