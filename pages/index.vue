<template>
  <div>
    <div class="project">
      <div class="container">
        <h1>プラットフォームサービスのエコシステム形成に関する実践的研究</h1>
        <v-card class="mx-auto project-card">
          <v-card-text>
            <p class="display-1 text--primary">
              Missoin.
            </p>
            <p>adjective</p>
            <div class="text--primary">
              well meaning and kindly.<br />
              "a benevolent smile"
            </div>
          </v-card-text>
          <v-card-actions>
            <v-btn text color="accent-4">
              Learn More
            </v-btn>
          </v-card-actions>
        </v-card>
        <v-card class="mx-auto project-card">
          <v-card-text>
            <p class="display-1 text--primary">
              Vision.
            </p>
            <p>adjective</p>
            <div class="text--primary">
              well meaning and kindly.<br />
              "a benevolent smile"
            </div>
          </v-card-text>
          <v-card-actions>
            <v-btn text color="accent-4">
              Learn More
            </v-btn>
          </v-card-actions>
        </v-card>
      </div>
    </div>
    <div class="activity">
      <div class="container">
        <h1>Activity.</h1>
        <v-carousel :show-arrows="false" interval="2000" progress="true">
          <v-carousel-item
            v-for="(item, i) in items"
            :key="i"
            :src="item.src"
          ></v-carousel-item>
        </v-carousel>
      </div>
    </div>
    <div class="profile">
      <div class="container">
        <h1>Profile.</h1>
        <v-slide-group v-model="model" class="pa-4" show-arrows>
          <v-slide-item
            v-for="n in 15"
            :key="n"
            v-slot:default="{ active, toggle }"
          >
            <v-card
              :color="active ? 'primary' : 'grey lighten-1'"
              class="ma-4"
              height="350"
              width="300"
              @click="toggle"
            >
              <v-row class="fill-height" align="center" justify="center">
                <v-scale-transition>
                  <v-icon
                    v-if="active"
                    color="white"
                    size="48"
                    v-text="'mdi-close-circle-outline'"
                  ></v-icon>
                </v-scale-transition>
              </v-row>
            </v-card>
          </v-slide-item>
        </v-slide-group>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
        },
        {
          src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
        },
      ],
      model: null,
    }
  },
}
</script>
<style scoped>
.project {
  background: -webkit-linear-gradient(to right, #36aa37 0%, #2da8aa 50%)
    no-repeat !important;
  background: linear-gradient(to right, #36aa37 0%, #2da8aa 50%) no-repeat !important;
}
.activity {
  background-color: #000000;
}
.profile {
  background: -webkit-linear-gradient(to right, #36aa37 0%, #2da8aa 50%)
    no-repeat !important;
  background: linear-gradient(to right, #36aa37 0%, #2da8aa 50%) no-repeat !important;
}
.project-card {
  margin: 50px;
  margin-left: 100px;
  text-align: center;
}
</style>
