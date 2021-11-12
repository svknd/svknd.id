<template>
  <v-app dark>
    <NavbarTwo />
    <v-main>
      <v-container fluid> 
        <Nuxt />
      </v-container>
        <v-footer padless>
    <v-col
      class="text-center"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>Rifki Ahmad Maulana</strong>
    </v-col>
  </v-footer>
    </v-main>
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
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>
<style>
  html{
    scroll-behavior: smooth;

  }
</style>