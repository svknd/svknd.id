<template>
  <div class="overflow-hidden">
    <main class="scroll-y">
      <v-parallax
        src="/home.png"
        style="height: 100vh;"
      >
        <v-overlay
          absolute
        >
          <v-row
            align="center"
            justify="center"
          >
            <v-col
              class="text-center"
            >
              <v-img
                src="/logo.png"
                alt="Logo Savikindo"
                max-width="200"
              ></v-img>
            </v-col>
          </v-row>
        </v-overlay>
      </v-parallax>
      <v-container
        style="height: 100vh;"
        fill-height
      >
        <v-row
          align="center"
          justify="center"
        >
          <v-col sm="6">
            <v-img src="https://via.placeholder.com/512x256"></v-img>
          </v-col>
          <v-col>
            <div class="my-2 title accent--text">Selamat Datang</div>
            <div class="display-1">Tentang Kami</div>
            <v-divider class="my-2"></v-divider>
            <div class="mb-2 subtitle">
              Kami adalah <i>Education Technology Startup</i> yang berpusat di Bandung, Indonesia.
            </div>
            <div class="subtitle">
              Produk kami berkonsentrasi pada sistem teknologi pendidikan yang dapat mengakomodir kebutuhan perkembangan pendidikan &amp; sesuai dengan format kebijakan yang diterbitkan oleh Kementerian Pendidikan dan Kebudayaan Indonesia.
            </div>
          </v-col>
        </v-row>
      </v-container>
    </main>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Home',
    }
  }
}
</script>

<style lang="scss">
.marquees {
  color: red;
  font-weight: bold;
}
</style>
