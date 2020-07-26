<template>
  <v-container>
    <h1>
      活動内容
    </h1>
    <v-layout>
      <div class="sentan">
        <v-card class="mx-auto" max-width="300">
          <v-img src="/activity/pin.jpg" height="200px"></v-img>

          <v-card-title>
            活動内容について
          </v-card-title>

          <v-card-subtitle>
            先端情報学実習って何するの？
          </v-card-subtitle>

          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn icon @click="showAct = !showAct">
              <v-icon>{{
                showAct ? 'mdi-chevron-up' : 'mdi-chevron-down'
              }}</v-icon>
            </v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="showAct">
              <v-divider></v-divider>

              <v-card-text>
                この先端情報学実習は、パンプラージュというアプリに関して、新しい機能を搭載したり、
                アプリ内に掲載する記事を作成し投稿したり、パンプラージュを多くの人に知ってもらえるよう
                広報活動をしたりします。このプロジェクトはだれでも参加できます！
                プログラミングに自信がない人でも大丈夫です！
                三年生や四年生の先輩方が、ホームページ作成やアプリ製作を一から教えてくださいます！
              </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </div>
      <div class="sentan">
        <v-card class="mx-auto" max-width="300">
          <v-img src="/activity/group.jpg" height="200px"></v-img>

          <v-card-title>
            グループワーク
          </v-card-title>

          <v-card-subtitle>
            半期をかけて一つの作品を制作する
          </v-card-subtitle>

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn icon @click="showGroup = !showGroup">
              <v-icon>{{
                showGroup ? 'mdi-chevron-up' : 'mdi-chevron-down'
              }}</v-icon>
            </v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="showGroup">
              <v-divider></v-divider>

              <v-card-text>
                この先端情報学実習を履修している学生を3つほどのグループに分けて、その小グループで目標
                を設定し、一つの作品を作り上げます！前期では、Web版パンプラージュの作成、記事投稿ページの
                リニューアル、先端情報学実習の紹介ページの作成を行いました。このグループワークを通して
                システム開発の基本を学んだり、前期で学んだ知識を実践的に活用していくことが出来ます！
              </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </div>
      <div class="sentan">
        <v-card class="mx-auto" max-width="300">
          <v-img src="/activity/adver.jpg" height="200px"></v-img>

          <v-card-title>
            チラシの掲示
          </v-card-title>

          <v-card-subtitle>
            パンプラージュの知名度向上
          </v-card-subtitle>

          <v-card-actions>
            <v-spacer></v-spacer>

            <v-btn icon @click="showAd = !showAd">
              <v-icon>{{
                showAd ? 'mdi-chevron-up' : 'mdi-chevron-down'
              }}</v-icon>
            </v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="showAd">
              <v-divider></v-divider>

              <v-card-text>
                前期の活動では、パンプラージュを多くの静岡大学に生徒に知ってもらおうと、
                4年生の先輩が作ってくださった広告を、メンバー自ら交渉し、静岡大学の生徒
                がよく利用するお店や施設に貼ってもらう活動を行いました。交渉の結果、
                かまどやさん(お弁当屋さん)や、ビッグデーさん(スーパー)に貼っていただくことが
                出来ました。
              </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </div>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    showAct: false,
    showGroup: false,
    showAd: false,
  }),
}
</script>
<style scoped>
.activity {
  background: -webkit-linear-gradient(to right, #36aa37 0%, #2da8aa 50%);
}
.sentan {
  margin: 40px 40px 40px 20px;
}
</style>
