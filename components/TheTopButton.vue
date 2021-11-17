<template>
  <v-btn
    :class="{'transform': scrollY < 32}"
    class="ma-3 ma-sm-5 transition"
    color="#FFC300"
    fixed
    fab
    bottom
    right
    small
    @click="scrollToTop"
  >
    <v-icon
      :class="{'transform': scrollY < 32}"
      class="transition"
    >mdi-chevron-up</v-icon>
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

<style>
.transform {
  transform: scale(0);
}

.transition {
  transition: all 0.3s;
}
</style>
