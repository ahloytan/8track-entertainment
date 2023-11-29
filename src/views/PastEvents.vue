<template>
  <div id="pastEvents">
    <div id="textHolder">
      <v-carousel hide-delimiters touch show-arrows="hover">
        <v-carousel-item :key="i" v-for="i in carousel">
          <v-layout row>
            <v-col xs4 :key="j" v-for="j in i" cols="3" class="pa-0">
              <v-img :src="getImageUrl(j.img)" alt=""></v-img>
            </v-col>
          </v-layout>
        </v-carousel-item>
      </v-carousel>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      carousel: 
        {
          0: [ 
            {
              img: '260.webp'
            },
            {
              img: '895.webp'
            },
            {
              img: 'herd2.webp'
            },
            {
              img: '2633.webp'
            },  
          ],
          1: [ 
            {
              img: '4173.webp'
            },
            {
              img: 'herd1.webp'
            },
            {
              img: '860.webp'
            },
            {
              img: '1156.webp'
            },  
          ],          
        }
      
    }
  },
  computed: {
    getImageUrl() {
      return (name) => {
        return new URL(`../assets/${name}`, import.meta.url).href
      }
    }
  }
}
</script>
<style scoped>
#pastEvents {
  position: relative;
  background-size: cover;
  background-position: center;
}

.v-carousel {
  height: auto !important;
}
</style>
