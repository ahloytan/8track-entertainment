<template>
  <v-container fluid id="upcomingEvents" class="pa-0">
    <div id="textHolder">
      <v-carousel hide-delimiters touch>
        <v-carousel-item
          v-for="item in carousel"
          :src="getImageUrl(item.background)"
          cover
        >
          <div class="content">
            <v-row no-gutters>
              <v-col class="fullCol d-flex flex-column justify-center align-center text-white" cols="12" md="6">
                <p class="text-h6 text-md-h5 py-10 kd">COMING SOON</p>
                <div>
                  <p class="text-h5 text-h2 kd font-weight-black">{{ item.eventTitle }}</p>
                </div>
              </v-col>
              <v-col class="text-white pa-8 pa-md-12">
                <div id="eventDetail" class="rounded-xl pa-8">
                  <div class="text-md-left">
                    <p class="text-h5 text-md-h4 kd">{{ item.eventTitle }}</p>
                    <p class="text-subtitle-1 text-md-h6 kd">{{ item.starring }}</p>
                    <p class="text-subtitle-1 text-md-h6 kd">{{ item.music }}</p>
                  </div>
                  <v-row class="my-10 text-md-left">
                    <v-col>
                      <div class="text-h4 text-md-h3 kd font-weight-bold">{{ item.startTime }}</div>
                      <div class="text-h6 text-md-h5 kd">START TIME</div>
                    </v-col>
                    <v-col>
                      <div class="text-h4 text-md-h3 kd font-weight-bold">{{ item.duration }}</div>
                      <div class="text-h6 text-md-h5 kd">DURATION</div>
                    </v-col>
                  </v-row>
                  <div class="text-subtitle-1 text-md-h6 kd">{{ item.location }}</div>
                  <div class="my-4">
                    <v-btn density="default" elevation="4" rounded="xl" class="text-white" size="x-large">BUY TICKETS</v-btn>
                  </div>
                </div>
              </v-col>
            </v-row>
          </div>
        </v-carousel-item>
      </v-carousel>
    </div>
  </v-container>
</template>
<script>
export default {
  data() {
    return {
      carousel: [
        {
          background: 'upcomingEvents.jpg',
          eventTitle: 'Freed Ballet',
          starring: 'Starring Nikka & Vitaly',
          music: 'Music By Dzmitry & Aisalu',
          startTime: '7:30PM',
          duration: '2HOURS',
          location: '22 May @ The Star Theatre'
        },
        {
          background: 'taeyeon.jpg',
          eventTitle: 'Taeyeon\'s Concert',
          starring: 'Starring Taeyeon',
          music: 'Music By Dzmitry & Aisalu',
          startTime: '8:30PM',
          duration: '2.5HOURS',
          location: '28 Mar @ Gardens By The Bay'
        },
        {
          background: 'ndp.jpg',
          eventTitle: 'National Day 2023',
          starring: 'Starring Sonia and Joakim',
          music: 'Music By Dzmitry & Aisalu',
          startTime: '5:30PM',
          duration: '4HOURS',
          location: '09 Aug @ The Padang'
        }
      ]
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
#eventDetail{
  background-color: rgba(255,255,255,0.25);
}


.v-carousel {
  height: auto !important;
}

.v-btn {
  background: linear-gradient(to right, #FF66C4, #CB6CE6);
}
</style>
