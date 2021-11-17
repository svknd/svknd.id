<template>
<v-app>
    <v-container>
      <div>
        <Home />
      </div>
    </v-container>
    <v-row>
      <Member />
    </v-row>
    <v-row>
      <Internship/>
    </v-row>
    <v-row>
      <Joinus />
    </v-row>

</v-app>
</template>

<script>
import Internship from '~/components/Internship.vue'
export default {
  components: { Internship },
  data() {
    return {
      smk: 'SMKN 13 BANDUNG',
      semangat: 'SEMANGAT MEREUN GAIS!!!',
    }
  },head() {
    return {
      title: "Landing Page"
    };
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
