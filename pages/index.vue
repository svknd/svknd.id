<template>
  <v-main class="black">
    <v-container class="pa-2 conCard " fluid fill-height>
      <v-row justify="space-around" align="center">
        
        <!-- Bagian 1 -->
        <v-col cols="12" sm="8" md="4" align-self="center">
            <v-card 
            class="px-5 py-1 mx-4"
            max-width="100%"
            color="black white--text">
                <h1>Welcome to the home of the Savikindo Tech</h1>
                <span>Kami adalah Education Technology Startup yang berpusat di Bandung, Indonesia</span>
            </v-card>

        </v-col>
        <v-col cols="auto">
          <v-img src="/welcome.jpg" width="610"></v-img>
        </v-col>
      </v-row>
    </v-container>

    <!-- Bagian 2 -->
    <v-container class="conCard white" fluid >
      <h1 class="cente">Tentang Kami</h1>
      <br>
      <v-row>
        <v-col cols="9" offset="3">
            <v-card width="650px">
              <p>Produk kami berkonsentrasi pada sistem teknologi pendidikan yang dapat mengakomodir kebutuhan perkembangan pendidikan & sesuai dengan format kebijakan yang diterbitkan oleh Kementerian Pendidikan dan Kebudayaan Indonesia.</p>
            </v-card>
        </v-col>
      </v-row>
      <br>
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
conCard {
  height: 600px;
  width: 400px;
}

cente {
  text-align: center;
}
</style>
