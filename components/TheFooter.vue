<template>
  <v-footer
    class="bg-primary"
    padless
  >
    <v-card
      flat
      tile
      width="100%"
      class="bg-primary text-center"
    >
      <v-card-text class="pt-0 pt-sm-3">
        <v-btn
          v-for="(link, i) in links"
          :key="i"
          :href="link.href"
          class="mx-4"
          target="_blank"
          icon
        >
          <v-icon class="text-primary">
            {{ link.icon }}
          </v-icon>
        </v-btn>
      </v-card-text>
      <v-card-text class="text-primary pt-0">
        &copy; {{ new Date().getFullYear() }} All rights reserved —
        <a class="text-decoration-none text-accent" href="/">
          <strong>Savikindo</strong>
        </a>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    links: [
      {
        icon: 'mdi-instagram',
        href: 'https://www.instagram.com/simak.indonesia/',
      },
      {
        icon: 'mdi-linkedin',
        href: 'https://www.linkedin.com/company/savikindo/',
      },
      {
        icon: 'mdi-youtube',
        href: 'https://www.youtube.com/channel/UC3THrxLuAEAhr0BiZEMjkew',
      },
    ],
  })
}
</script>

<style>
.text-primary {
  color: #FFFFFF7F!important;
}

.bg-primary {
  background-color: #2C2C2C!important;
}

.text-accent {
  color: #FFC300!important;
}
</style>
