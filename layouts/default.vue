<template>
  <v-app>
    <Header />
    <v-content>
      <nuxt />
    </v-content>
    <Footer />
  </v-app>
</template>
<script>
import Header from '@/components/header.vue'
import Footer from '@/components/footer.vue'
export default {
  components: {
    Header,
    Footer,
  },
}
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Kosugi+Maru&display=swap');
#app {
  font-family: 'Kosugi Maru', sans-serif;
}
</style>
