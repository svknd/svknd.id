<template>
  <v-container
    :id="$vuetify.breakpoint.name !== 'xs' ? 'screen-height' : ''"
    align="center"
    fill-height
  >
    <v-row
      id="container-image"
      align="center"
      justify="space-between"
    >
      <v-col
        style="background: #FFFFFF7F"
        cols="12"
        sm="5"
      >
        <h2 class="text-right text-sm-left">Hubungi Kami</h2>
        <v-divider
          class="mt-1 mb-5"
        ></v-divider>
        <v-container>
          <v-row
            class="mb-3"
            align="center"
          >
            <v-col cols="auto">
              <v-icon
                class="pa-3 mr-1 grey lighten-3"
              >mdi-map-marker</v-icon>
            </v-col>
            <v-col>
              <span>
                Jl. Kanayakan Lama No 40, Dago, Coblong, Bandung
                Jawa Barat, Indonesia – 40135
              </span>
            </v-col>
          </v-row>
          <v-row
            class="mb-3"
            align="center"
          >
            <v-col cols="auto">
              <v-icon
                class="pa-3 mr-1 grey lighten-3"
              >mdi-email</v-icon>
            </v-col>
            <v-col>
              <span>info@savikindo.co.id</span>
            </v-col>
          </v-row>
          <v-row align="center">
            <v-col cols="auto">
              <v-icon
                class="pa-3 mr-1 grey lighten-3"
              >mdi-phone</v-icon>
            </v-col>
            <v-col>
              <span>(022) 2027 8381</span>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
      <v-col
        class="pa-5 grey lighten-4"
        cols="12"
        sm="4"
      >
        <form>
          <h2>Kirim Pesan</h2>
          <v-text-field
            label="Nama"
            :rules="nama"
          ></v-text-field>
          <v-text-field
            label="Email"
            type="email"
            :rules="email"
          ></v-text-field>
          <v-text-field
            label="No. HP"
            :rules="telepon"
          ></v-text-field>
          <v-textarea
            label="Pesan"
            :rules="pesan"
          ></v-textarea>
          <v-btn
            class="green lighten-1"
            type="submit"
          >Kirim</v-btn>
          <v-btn
            class="amber"
            type="reset"
          >Reset</v-btn>
        </form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  head() {
    return {
      title: 'Join Us',
    }
  },
  data() {
    return {
      nama: [
        value => !!value || 'Wajib terisi',
        value => (value || '').length <= 20 || 'Maksimal 20 karakter',
      ],
      email: [
        value => !!value || 'Wajib terisi',
        value => {
          const pattern = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
          return pattern.test(value) || 'E-mail tidak valid'
        },
      ],
      telepon: [
        value => !!value || 'Wajib terisi',
        value => (value || '').length <= 13 || 'Nomor melebihi batas wajar',
        value => {
          const pattern = /08\d+/
          return pattern.test(value) || 'Nomor HP tidak valid'
        }
      ],
      pesan: [
        value => !!value || 'Wajib terisi'
      ]
    }
  }
}
</script>

<style>
#container-image {
  background: linear-gradient(0deg, #FFFFFF7F, #FFFFFF7F), url('/join.jpg');
  background-size: auto 100%;
}

#screen-height {
  height: 100vh;
}
</style>
