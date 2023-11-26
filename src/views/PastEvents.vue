<template>
  <div id="pastEvents">
    <div id="textHolder" class="alignCenter">
      <img :src="imgSource">
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
    }
  },
  computed: {
    imgSource() {
      let image = 'pE1';
      if (window.innerWidth <= 420) image = 'pE2';
      return new URL(`../assets/${image}.png`, import.meta.url).href
    }
  }
}
</script>
<style scoped>
#pastEvents {
  position: relative;
  background-image: url('../assets/pastEvents.jpg');
  background-size: cover;
  background-position: center;
  height: 100vh;
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
</style>
