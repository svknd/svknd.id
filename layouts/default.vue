<template>
  <v-app dark>
    
    <!-- Komponen Navbar -->
    <Navbar />

  <v-main>
    <Nuxt />
  </v-main>
      
    <!-- Footer -->
    <v-footer height="auto" class="black" padless> 

    <v-container class="grey darken-4 mx-0 my-0" fluid>
      <v-row>
        <v-col cols="3" offset="3">
          <div class="child">
            <h4 class="text-center">Hubungi Kami</h4>
            <br>
              <p class="pl-7"> <v-icon>mdi-phone</v-icon> : (022) 2027 8381</p>
              <p class="pl-7"> <v-icon>mdi-nfc-search-variant</v-icon> : info@savikindo.co.id</p>
              <v-btn
            v-for= "(button,i) in buttons"
            :key= "i"
            :href= "button.link"
            target="_blank"
            class="mx-4 pl-9"
            icon
            >
              <v-icon>
                {{ button.icon }}
              </v-icon>
            </v-btn>
          </div>  
        </v-col>
        
        <v-col cols="6">      
          <div class="child">
            <h4 class="text-center">Alamat</h4>
            <br>
            <p class="pl-1">Jl. Kanayakan Lama No.40, Dago, Kecamatan Coblong, Kota Bandung, Jawa Barat 40135</p>
          </div> 
        </v-col>  
      </v-row>
      <v-row>
        <v-col class="pa-0">
      <v-card class="d-flex justify-center black">
      <p class="white--text text-center my-3">
        Savikindo tech ||
          <span class="color">&copy; {{ new Date().getFullYear() }}</span>
        All Right Reserved
      </p>
    </v-card>
    </v-col>
    </v-row>
    </v-container>

    
    </v-footer>

  </v-app>

</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      buttons: [
           {
        icon: 'mdi-instagram',
        link: 'https://www.instagram.com/simak.id/',
        },
      {
        icon: 'mdi-linkedin',
        link: 'https://www.linkedin.com/company/savikindo/',
       },
      {
        icon: 'mdi-youtube',
        link: 'https://www.youtube.com/channel/UC3THrxLuAEAhr0BiZEMjkew',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>

<style scoped>
.child {
  width: 250px;
}
.cwhite {
  color: white;
  text-align: center;
}
.position {
  align-items: center;
}
</style>