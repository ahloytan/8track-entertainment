<template>
  <div id="tabs">
    <v-container fluid class="bg-surface-variant pa-0">
        <v-row no-gutters>
            <v-col
                v-for="tab in tabs"
                :key="tab"
                cols="12"
                sm="4"
            >
              <v-sheet class="mx-0 sheet">
                <v-img
                    class="images"
                    :aspect-ratio="1.75"
                    cover
                    :src="getImageUrl(tab.img)"
                    :alt="tab.title"
                ></v-img>       
                <v-icon :icon="'mdi-' + tab.icon" class="alignCenter icons" color="white"></v-icon>
                <span class="alignCenter title text-white text-h6">{{ tab.title }}</span> <!--  text-xl-h4 -->
                <v-divider :thickness="2" class="alignCenter line border-opacity-100"></v-divider>
                <span class="alignCenter learnMore text-white text-subtitle-2">LEARN MORE</span> <!--  text-xl-h6 -->
              </v-sheet>
            </v-col>
        </v-row>
    </v-container>
  </div>
</template>
<script setup>

const tabs = [
  {
    title: "About Us",
    img: "zoukOut",
    icon: "information-outline"
  }, 
  {
    title: "Upcoming Events",
    img: "bp",
    icon: "calendar-month-outline"
  },
  {
    title: "Past Events",
    img: "ts",
    icon: "calendar-multiple-check"
  }
]
const getImageUrl = (name) => {
    return new URL(`../assets/${name}.jpg`, import.meta.url).href
}
</script>



<style scoped>
span {
  font-family: "KudryashevDisplay" !important;
}

.images {
  filter: brightness(75%);

  &:hover {
    filter: brightness(100%);
  }
}

.sheet {
  position: relative;
}

.icons {
  top:25%;
  font-size: 40px;
}

.line {
  width: 25%;
  bottom: 30%;
  color: orangered;
}

.learnMore {
  bottom:20%;
}

.title {
  top:50%;
}

.alignCenter {
  position:absolute;
  display:block;
  left:0;
  right:0;
  margin:auto;
  z-index: 99;
}

@media only screen and (min-width: 1400px) {
  .icons {
    top:25%;
    font-size: 60px;
  }

}
</style>
