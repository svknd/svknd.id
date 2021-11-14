<template>
  <v-main class="pa-0">
    <v-container 
    class="pt-16 black" 
    fluid>
      <v-row justify="space-around" align="center">
        
        <!-- Bagian 1 -->
        <v-col cols="12" sm="8" md="4" align-self="center">
            <v-card 
            class="px-5 py-1 mx-4"
            max-width="100%"
            color="black white--text">
                <h1 class="mb-5 text-h5 text-sm-h4">Welcome to the home of Savikindo Tech</h1>
                <hr class="mb-2">
                <span class="text-subtitle-1">Kami adalah Education Technology Startup yang berpusat di Bandung, Indonesia</span>
            </v-card>

        </v-col>
        <v-col cols="auto">
          <v-img src="/welcome.jpg" width="610"></v-img>
        </v-col>
      </v-row>
    </v-container>

    <!-- Bagian 2 -->
    <v-container class="white">
      <br>
      <v-row justify="center" align="center" >
        <v-col cols="auto">
          <v-img src="our.svg" height="200px" width="200px"></v-img>
        </v-col>
        <v-col  cols="10" >
             <div class="mb-2 text-h4 text-center ">
              Tentang Kami
            </div>
            <div class="subtitle 1 text-center text-xs-caption">
              Produk kami berkonsentrasi pada sistem teknologi pendidikan yang dapat mengakomodir kebutuhan perkembangan pendidikan &amp; sesuai dengan format kebijakan yang diterbitkan oleh Kementerian Pendidikan dan Kebudayaan Indonesia.
            </div>
        </v-col>
      </v-row>
    </v-container>
  </v-main>
</template>

<script>
export default {
 
}
</script>

<style lang="scss">
.marquees {
  color: red;
  font-weight: bold;
}
h1 {
  text-align: center;
}

</style>
