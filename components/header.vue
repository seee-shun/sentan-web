<template>
  <div>
    <v-card class="overflow-hidden" width="800">
      <v-app-bar
        :collapse="!collapseOnScroll"
        :collapse-on-scroll="collapseOnScroll"
        color="black"
        dark
        app
        scroll-target="#scrolling-techniques-6"
      >
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

        <v-toolbar-title>先端</v-toolbar-title>

        <v-spacer></v-spacer>
      </v-app-bar>
      <v-navigation-drawer v-model="drawer" temporary fixed>
        <v-list nav dense>
          <v-list-item-group
            v-model="group"
            active-class="black--text text--accent-4"
          >
            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-home</v-icon>
              </v-list-item-icon>
              <v-list-item-title
                ><nuxt-link to="/">Top</nuxt-link></v-list-item-title
              >
            </v-list-item>
            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-laptop</v-icon>
              </v-list-item-icon>
              <v-list-item-title
                ><nuxt-link to="/detailActivity"
                  >Activity</nuxt-link
                ></v-list-item-title
              >
            </v-list-item>

            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-account</v-icon>
              </v-list-item-icon>
              <v-list-item-title
                ><nuxt-link to="/detailProfile"
                  >Profile</nuxt-link
                ></v-list-item-title
              >
            </v-list-item>

            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-alpha-y-circle</v-icon>
              </v-list-item-icon>
              <v-list-item-title
                ><a href="www.yuhashi-lab.net">遊橋研究室</a></v-list-item-title
              >
            </v-list-item>
            <v-list-item>
              <v-list-item-icon>
                <v-icon>mdi-alpha-s-circle</v-icon>
              </v-list-item-icon>
              <v-list-item-title
                ><a href="www.sugilab.net/2020/index.html"
                  >杉山研究室</a
                ></v-list-item-title
              >
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
      <v-sheet
        id="scrolling-techniques-6"
        class="overflow-y-auto"
        max-height="600"
      >
      </v-sheet>
    </v-card>
  </div>
</template>
<script>
export default {
  data: () => ({
    drawer: false,
    collapseOnScroll: true,
  }),
}
// collapseとcollapse-on-scroll propsを使う
</script>
