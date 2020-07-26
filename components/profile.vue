<template>
  <div class="profile">
    <div class="container">
      <h1>Profile.</h1>
      <!-- <v-sheet class="mx-auto" elevation="8" max-width="800"> -->
      <v-slide-group v-model="model" class="pa-4" center-active show-arrows>
        <v-slide-item
          v-for="(item, n) in items"
          :key="n"
          v-slot:default="{ active, toggle }"
        >
          <v-card
            :color="active ? 'white' : 'white'"
            class="ma-4"
            height="300"
            width="210"
            @click="toggle"
          >
            <v-img src="~/assets/profile/noimage.jpg" height="200px"></v-img>

            <v-card-title>{{ item.name }}</v-card-title>

            <v-card-subtitle color="black">{{ item.subname }}</v-card-subtitle>

            <v-row class="fill-height" align="center" justify="center">
              <v-scale-transition>
                <v-icon
                  v-if="active"
                  color="black"
                  size="48"
                  v-text="'mdi-close-circle-outline'"
                ></v-icon>
              </v-scale-transition>
            </v-row>
          </v-card>
        </v-slide-item>
      </v-slide-group>
      <!-- </v-sheet> -->
    </div>
  </div>
</template>
<script>
export default {
  data: () => ({
    item: 1,
    items: [
      { name: '清野 峻吾', subname: 'Seino Syungo', picture: '' },
      { name: '渡辺 大誠', subname: 'Watanabe Taisei', picture: '' },
      { name: '梶 貴広', subname: 'Kaji Takahiro', picture: '' },
      { name: '城崎 遼', subname: 'Josaki Ryo', picture: '' },
      { name: '小塚 公介', subname: 'Kozuka Kosuke', picture: '' },
      { name: '和田 颯太郎', subname: 'Wada Sotaro', picture: '' },
      { name: '森岡 美冴', subname: 'Morioka Miki', picture: '' },
      { name: 'Nguyen Thuy Duong', subname: 'Nguyen Thuy Duong', picture: '' },
      { name: '江原 柊太', subname: 'Ebara Syuta', picture: '' },
      { name: '赤熊 佑斗', subname: 'Akakuma Yuto', picture: '' },
      { name: '山口 翼', subname: 'Yamaguti Tubasa', picture: '' },
      { name: '表 梨花子', subname: 'Omote Rikako', picture: '' },
      { name: '鶴﨑 弘晃', subname: 'Tsurusaki Hiroaki', picture: '' },
    ],
  }),
}
</script>
