<template class="overflow-hidden">
  <div class="overflow-hidden">
    <v-main>
      <navbar />

      <v-parallax src="/desk.jpg" style="height: 100vh">
        <v-card-title
          class="text-center justify-center"
          style="margin-top: -100px"
        >
          <v-text class="white--text">
            <font class="text-h2 font-weight-light" style="word-break:normal;">Internship</font>
            <br />

            <font
              class="text-subtitle 1 font-weight-light"
              style="word-break: normal"
              >Lorem ipsum dolor sit amet constrectur aba
            </font>
          </v-text>
        </v-card-title>
      </v-parallax>

      <v-container style="margin-top: -250px">
        <v-row align="center" justify="center">
          <template v-for="(item, i) in items">
            <v-col :key="i" cols="12" md="4" sm="4">
              <v-card class="elevation-4">
                <v-img src="https://picsum.photos/500/400?image"> </v-img>
                <v-card-text class="pt-6" style="position: relative">
                  <v-text class="text-h6 font-weight-light mb-2">
                    {{ item.year }}
                  </v-text>
                  <h4 class="text-h4 font-weight-light" style="color: #d8a200">
                    {{ item.name }}
                  </h4>
                  <h3 class="text-h6 font-weight-light mb-3">
                    {{ item.school }}
                  </h3>
                  <div class="font-weight-light text-h6 mb-2">
                    {{ item.impression }}
                  </div>
                  <div>
                    <v-btn icon target="blank" :href="item.instagram">
                      <v-icon style="color: #ead73b">mdi-instagram</v-icon>
                    </v-btn>
                    <v-btn icon target="blank" :href="item.linkedin">
                      <v-icon style="color: #ead73b">mdi-linkedin</v-icon>
                    </v-btn>
                    <v-btn icon :href="item.github">
                      <v-icon style="color: #ead73b">mdi-github</v-icon>
                    </v-btn>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
          </template>
        </v-row>
      </v-container>
    </v-main>
  </div>
</template>
<script>
export default {
  data() {
    return {
      dialog: false,
      notifications: false,
      sound: true,
      widgets: false,

      items: [
        {
          name: 'Cikal Gemintang Seya',
          year: '2021',
          img: '',
          school: 'SMKN 13 Bandung',
          impression: '"Aku sangat senang karena aku sangat senang"',
          instagram: 'https://www.instagram.com/ckl_gs/?hl=id',
          linkedin: 'https://www.linkedin.com/in/cikal-gs/',
          github: 'https://github.com/sglkc',
        },
        {
          name: 'Fadhil Maulana',
          year: '2021',
          img: '',
          school: 'SMKN 13 Bandung',
          impression: '"Aku sangat belajar banyak disini , aku jadi senang"',
          instagram: '',
          linkedin: '',
          github: '',
        },
        {
          name: 'M Irsyaad Fatahilah',
          year: '2021',
          img: '',
          school: 'SMKN 13 Bandung',
          impression: '"Disini orang orangnya sangat humble , aku jadi nyaman"',
          instagram: 'https://www.instagram.com/irsyaad_06/?hl=id',
          linkedin: 'https://www.linkedin.com/in/irsyaad-fatahilah-906b64214/',
          github: 'https://github.com/irsyaad06',
        },
        {
          name: 'Rifki Ahmad Maulana',
          year: '2021',
          img: '',
          school: 'SMKN 13 Bandung',
          impression: '"Aku banyak belajar disini!" ',
          instagram: '',
          linkedin: '',
          github: '',
        },
      ],

      transparent: 'rgba(255, 255, 255, 0)',
    }
  },
  head() {
    return {
      title: 'Home',
      overlay: false,
    }
  },
}
</script>

<style>
::selection {
  background: #ffc300;
}
</style>