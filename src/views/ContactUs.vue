<template>
  <div id="contactUs">
    <v-layout id="footer">
      <v-footer class="justify-center dark py-12">
        <v-row justify="center" no-gutters>
          <v-col cols="12">
            <div class="dark kd text-white">Let's Connect</div>
          </v-col>
          <v-col cols="12" class="mb-4">
            <a v-for="icon in icons" :href="icon.link" target="_blank">
              <v-btn
                :key="icon"
                class="mx-4"
                :icon="icon.icon"
                color="white"
                variant="text"
              ></v-btn>
            </a>
          </v-col>
          <v-col cols="12">
            <div class="dark kd text-white">Email@8track.co</div>
            <div class="dark kd text-white">7 Temasek Boulevard Suntec Tower One #12-07 Singapore 038987</div>
          </v-col>
          <v-col cols="12" class="mt-4">
            <div class="dark kd text-white">Coded by <a target="_blank" href="https://ahloytan.netlify.app" class="text-decoration-underline">ahloytan</a></div>
          </v-col>
        </v-row>
      </v-footer>
    </v-layout>
  </div>
</template>
<script>
  export default {
    data: () => ({
      icons: [
        {
          icon: 'mdi-instagram',
          link: 'https://www.instagram.com/ahloytan/',
        },
        {
          icon: 'mdi-facebook',
          link: 'https://www.facebook.com/ATJH4',
        },
        // {
        //   icon: 'mdi-twitter',
        //   link: 'https://twitter.com/itsmeahloy',
        // },
        // {
        //   icon: 'mdi-linkedin',
        //   link: 'https://www.linkedin.com/in/aloytan/',
        // },
    
      ],
    }),
  }
</script>

<style scoped>
.fullCol {
  height: 100vh;
}

.content {
  min-height: 100%;
}

.dark { 
  background-color: #1C1919 !important; 
}
</style>
