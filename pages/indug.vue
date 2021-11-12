<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card class="px-8 py-5">
        <NuxtLogo />
        <VuetifyLogo />
        <h2 class="py-10 text-center">Selamat datang {{ smk }}</h2>
        <p>Semangatnya bikin landing pagenya!</p>
        <p class="mb-0">Referensi website it company :</p>
        <a href="https://www.xtremax.com" target="_blank"
          >https://www.xtremax.com</a
        >
        <a href="https://www.efishery.com/" target="_blank"
          >https://www.efishery.com/
        </a>
        <a href="https://www.mitrais.com/" target="_blank"
          >https://www.mitrais.com/</a
        >
        <a href="https://www.voxteneo.com/" target="_blank"
          >https://www.voxteneo.com/</a
        >

        <p class="mb-0 mt-4">Referensi landing page yg bagus banyak disini :</p>
        <a href="https://themeforest.net/" target="_blank"
          >https://themeforest.net/</a
        >

        <p class="mb-0 mt-4">
          Referensi icon atau image buat di halaman website :
        </p>
        <a href="https://undraw.co/" target="_blank">https://undraw.co/ </a>
        <a href="https://www.flaticon.com/ " target="_blank"
          >https://www.flaticon.com/
        </a>
        <a href="https://unsplash.com/" target="_blank"
          >https://unsplash.com/</a
        >

        <p class="mb-0 mt-4">ini website nuxt :</p>
        <a href="https://nuxtjs.org/" target="_blank">https://nuxtjs.org/</a>

        <p class="mb-0 mt-4">
          ini website vuetify buat component sama cssnya :
        </p>
        <a href="https://vuetifyjs.com/en/" target="_blank"
          >https://vuetifyjs.com/en/</a
        >

        <marquee behavior="" direction="" class="marquees mt-10">{{
          semangat
        }}</marquee>
      </v-card>
    </v-col> 
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      smk: 'SMKN 13 BANDUNG',
      semangat: 'SEMANGAT MEREUN GAIS!!!',
    }
  },
  computed: {
    // ini buat bikin data yg reactive
  },
  mounted() {
    // ini biasanya buat manggil fungsi di method yg harus di panggil di awal page di load
  },
  methods: {
    // ini buat function event
  },
}
</script>

<style lang="scss">
.marquees {
  color: red;
  font-weight: bold;
}
</style>
