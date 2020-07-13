<template>
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
</template>
<script>
export default {
  data() {
    return {
      model: null,
    }
  },
}
</script>
