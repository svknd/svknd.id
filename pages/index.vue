<template class="overflow-hidden">
  <div class="overflow-hidden">
    <v-main class="scroll-y">
      <navbar />

      <v-parallax src="/home.png" style="height: 100vh">
        <v-overlay absolute>
          <v-container>
            <v-row>
              <v-col align="center" class="">
                <h1>Welcome to the<br />home of the<br />#Savikindo tech</h1>
              </v-col>
            </v-row>
          </v-container>
        </v-overlay>
      </v-parallax>

      <v-container fill-height style="height: 100vh" class="my-md-16 my-lg-5">
        <v-row>
          <v-col>
            <v-text class="text-h2 font-weight-medium">
              <font color="#f2d516">HI THERE!</font> <br />
              <font class="text-h3 font-weight-light"> ABOUT US </font>
            </v-text>
            <br />
            <br />
            <br />
            <v-text class="text-body-1">
              We are an Education Technology Startup based in Bandung,
              Indonesia.
              <br />
              <br />

              Our product concentrates on an educational technology system that
              can accommodate the needs of educational development & is in
              accordance with the policy format published by the Indonesian
              Ministry of Education and Culture.
              <br />
              <br />
              <br />
              <br />

              We are Team of
              <a
                href="https://savikindo.co.id/index.php"
                target="blank"
                class="text-decoration-none"
                >Savikindo</a
              >
            </v-text>
          </v-col>
          <v-col cols="6" class="d-none d-lg-flex d-xl-none">
            <v-img src="ys.jpg" class="z-index:1;"></v-img>
          </v-col>
        </v-row>
      </v-container>

      <v-container
        class="text-center mb-16"
        style="height: auto; padding-top: 10px"
      >
        <v-text class="text-h2" style="z-index: 10"
          >Our product<br />
          <br />
        </v-text>

        <v-row align="center" justify="center">
          <template v-for="(item, i) in items">
            <v-col :key="i" cols="12" md="4">
              <v-hover v-slot="{ hover }">
                <v-card>
                  <v-img :src="item.img" height="400px">
                    <v-card-title
                      class="text-h5 white--text elevation-6"
                      align="center"
                      justify="center"
                    >
                      <v-row class="d-flex" justify="center" align="center">
                        <v-text class="text mt-4 pb-4">
                          {{ item.title }}
                        </v-text>

                        <div class="align-self-center pt-4"></div>
                      </v-row>
                    </v-card-title>
                    <v-fade-transition>
                      <v-overlay v-if="hover" absolute color="#036358">
                        <v-btn
                          :class="{ 'show-btns': hover }"
                          :color="transparent"
                          :href="item.link"
                          target="blank"
                        >
                          {{ item.sublink }}
                        </v-btn>
                      </v-overlay>
                    </v-fade-transition>
                  </v-img>
                </v-card>
              </v-hover>
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
          title: 'Simak.id',
          text: 'Tap to continue to product',
          img: 'home.png',
          sublink: 'Go to Product',
          link: 'https://simak.id/',
        },
        {
          title: 'Simak.Pay',
          text: 'Tap to continue to product',
          img: 'aboutus.jpg',
          sublink: 'Go to Product',
          link: 'error.vue',
        },
        {
          title: 'Belajarbareng.id',
          text: 'Tap to continue to product',
          img: 'desk.jpg',
          sublink: 'Go to Product',
          link: 'https://www.belajarbareng.id/',
        },
        {
          title: 'Coming Soon',
          text: 'Tap to continue to product',
          img: 'ys.jpg',
          sublink: 'Go to Product',
          link: 'error.vue',
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



<style scoped>
.show-btns {
  color: rgba(255, 255, 255, 1) !important;
}
::selection {
  background: #ffc300;
}
</style>



