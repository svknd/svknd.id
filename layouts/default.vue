<template>
  <v-app dark>
    <v-main>
<<<<<<< HEAD
      <v-container>
        <Nuxt />
      </v-container>
=======
      <v-container fluid class="pa-0">
        <Nuxt />
        
      </v-container>
      
>>>>>>> 52784ee (Home Page)
    </v-main>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
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
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js',
    }
  },
}
</script>
<<<<<<< HEAD
=======

<style scoped>
  v-main{
    
  }
</style>
>>>>>>> 52784ee (Home Page)
