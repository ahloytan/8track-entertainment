
<template>
  <v-tabs
    v-model="tab"
    color="white"
    align-tabs="center"
    mobile-breakpoint="sm"
  >
    <v-tab v-for="tab in tabs" :value="tab.id" class="text-white" @click="goToSection(tab.id)">
      {{ tab.title }}
    </v-tab>
    
  </v-tabs>
</template>
<script>
  export default {
    data: () => ({
      tab: null,
      tabs: [
        {
          title: "About Us",
          id: 'aboutUs'
        }, 
        {
          title: "Upcoming Events",
          id: 'upcomingEvents'
        },
        {
          title: "Past Events",
          id: 'pastEvents'
        }
      ]
    }),
    methods: {
      goToSection(section) {
        var targetSection = document.getElementById(section);
        this.tab = section;
        targetSection.scrollIntoView({ behavior: 'smooth' });
      }
    }
  }
</script>
<style scoped>
.v-btn--outlined {
    border: none;
  }
</style>