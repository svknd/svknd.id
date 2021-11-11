<template>
  <v-btn
    :class="{'d-none': scrollY < 32}"
    class="ma-3 ma-sm-5"
    color="#FFC300"
    fixed
    fab
    bottom
    right
    small
    @click="scrollToTop"
  >
    <v-icon>mdi-chevron-up</v-icon>
  </v-btn>
</template>

<script>
export default {
  data() {
    return {
      scrollY: 0,
    }
  },
  beforeMount() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll () {
      this.scrollY = window.scrollY;
    },
    scrollToTop() {
      window.scrollTo({
        top: 0,
        left: 0,
        behavior: 'smooth'
      });
    }
  }
}
</script>
