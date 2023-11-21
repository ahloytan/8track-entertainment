<template>
  <div id="contactUs">
    <div class="content">
      <v-row no-gutters>
        <v-col class="fullCol d-flex flex-column justify-center align-center text-white" cols="12" md="6">
          <p class="text-h4 text-md-h2 py-14 ">Contact Us</p>
          <div>
            <p class="text-h6 text-md-h4 py-4">Phone: 9876 5432</p>
            <p class="text-h6 text-md-h4 py-4">Telegram: @ahloysius</p>
            <p class="text-h6 text-md-h4 py-4">Email: aloysius@gmail.com</p>
          </div>
        </v-col>
        <v-col>
        </v-col>
      </v-row>
    </div>
    <v-layout id="footer">
      <v-footer class="justify-center">
        <a v-for="icon in icons" :href="icon.link" target="_blank">
          <v-btn
            :key="icon"
            class="mx-4"
            :icon="icon.icon"
            color="white"
            variant="text"
          ></v-btn>
        </a>
      </v-footer>
    </v-layout>
  </div>
</template>
<script>
  export default {
    data: () => ({
      icons: [
        {
          icon: 'mdi-facebook',
          link: 'https://www.facebook.com/ATJH4',
        },
        {
          icon: 'mdi-twitter',
          link: 'https://twitter.com/itsmeahloy',
        },
        {
          icon: 'mdi-linkedin',
          link: 'https://www.linkedin.com/in/aloytan/',
        },
        {
          icon: 'mdi-instagram',
          link: 'https://www.instagram.com/ahloytan/',
        }
      
      ],
    }),
  }
</script>

<style scoped>

#contactUs {
  background-image: url('../assets/contactUs.png');
  background-size: cover;
  background-position: center, center;
  height: 100vh;
  width: 100vw;
}

p {
  font-family: "Kudryashev Display Sans" !important;
}

.fullCol {
  height: 100vh;
}

.content {
  min-height: 100%;
}

.v-footer { 
  background-color: #1C1919 !important; 
}
</style>
