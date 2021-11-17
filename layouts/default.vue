<template>
  <v-app dark>
    <v-main>
      <v-container fluid class="pa-0">
        <Nuxt />
        
      </v-container>
     <v-footer style="background-color: #2c2c2c; height:auto" class="mt-16">
        <v-container>
          <v-row justify="center" align="center">
            <v-col justify="left" align="left" class="white--text">
              <h1 class="text-h5 font-weight-medium mt-10">Our Product :</h1>
              <a href="https://simak.id/"
                ><v-img
                  src="/simakid.png"
                  max-width="200px"
                  class="mt-9"
                ></v-img
              ></a>
              <a href="https://www.belajarbareng.id/">
                <v-img src="/belajarbareng.png" max-width="250px" class="mt-8">
                </v-img
              ></a>
            </v-col>
            <v-col justify="left" align="left" class="white--text">
              <h1 class="text-h5 font-weight-medium " style="margin-top:-80px;" >Chat us :</h1>
              <a
                href="https://api.whatsapp.com/send/?phone=6285157157855&text&app_absent=0"
                target="blank"
                class="text-decoration-none"
                ><v-icon class="mt-n2 mr-2" style="color:#F2D516">mdi-mail</v-icon>
                <font color="white"> info@savikindo.co.id </font>
               </a>
               <br>
                <a
                href="mailto:info@savikindo.co.id"
                target="blank"
                class="text-decoration-none"
                ><v-icon class="mt-n2 mr-2" style="color:#F2D516">mdi-whatsapp</v-icon>
                <font color="white"> +6285157157855 </font>
               </a>
            </v-col>
           
             <v-col justify="left" align="left" class="white--text">
              <h1 class="text-h5 font-weight-medium " style="margin-top:-80px;" >Follow us</h1>
              <a
                href="https://www.youtube.com/c/SIMAKIndonesia/featured"
                target="blank"
                class="text-decoration-none"
                ><v-icon class="mt-n2 mr-2" style="color:#F2D516">mdi-youtube</v-icon>
                <font color="white">Simak Indonesia </font>
               </a>
               <br>
                <a
                href="https://www.instagram.com/simak.id/"
                target="blank"
                class="text-decoration-none"
                ><v-icon class="mt-n2 mr-2" style="color:#F2D516">mdi-instagram</v-icon>
                <font color="white">Simak Indonesia </font>
               </a>
            </v-col>
           
          </v-row>
        </v-container>
      </v-footer>
    </v-main>
     
  </v-app>
</template>

  

<style scoped>
</style>