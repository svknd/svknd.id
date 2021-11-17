<template class="overflow-hidden">
  
    <v-img src="/building2.png">
      <v-main>
        <navbar />

        <v-container fluid style="height: auto; padding-top: 125px">
          <v-card-title class="text-center justify-center py-6">
            <v-text class="white--text">
              <font class="text-h6"> Members ;</font>
              <br />
              <font class="text-h2 font-weight-light" style="word-break: normal"
                >Meet Our Team
              </font>
              <br />
              <font class="text-subheader 1 font-weight-light"
                >We are team Of
                <a
                  href="https://savikindo.co.id/about.php#"
                  style="color: #ead73b"
                  class="text-decoration-none font-weight-medium"
                  >Savikindo</a
                ></font
              >
            </v-text>
          </v-card-title>
          <v-container class="mt-7">
            <v-content>
              <v-container fluid fill-height px-3 py-1>
                <v-fade-transition leave-absolute>
                  <v-container fluid fill-height pa-0 ma-0>
                    <v-layout column>
                      <v-flex>
                        <v-tabs
                          v-model="tab"
                          dark
                          background-color="transparent"
                          color="yellow"
                          grow
                          show-arrows=""
                          class="mb-16"
                        >
                          <v-tab v-for="tabname in tabnames" :key="tabname">
                            {{ tabname }}
                          </v-tab>
                        </v-tabs>
                        <v-tabs-items
                          v-model="tab"
                          style="background-color: rgba(30, 30, 30, 0)"
                        >
                          <v-card style="background-color: rgba(30, 30, 30, 0)">
                            <v-tab-item
                              v-for="n in 8"
                              :key="n"
                              style="background-color: rgba(30, 30, 30, 0)"
                            >
                              <v-container fluid>
                                <v-row>
                                  <v-col
                                    v-for="i in 6"
                                    :key="i"
                                    cols="12"
                                    md="4"
                                  >
                                    <v-hover v-slot="{ hover }">
                                      <v-card
                                        class="mx-auto"
                                        color="grey lighten-4"
                                        max-width="400"
                                        :elevation="hover ? 12 : 1"
                                      >
                                        <v-img
                                          :src="`https://picsum.photos/500/300?image=${
                                            i * n * 5 + 10
                                          }`"
                                          :lazy-src="`https://picsum.photos/10/6?image=${
                                            i * n * 5 + 10
                                          }`"
                                          :aspect-ratio="16 / 16"
                                        ></v-img>
                                        <v-card-text
                                          class="pt-6"
                                          style="position: relative"
                                        >
                                          <h3
                                            class="
                                              text-h4
                                              font-weight-light
                                              mb-2
                                            "
                                            style="color: #d8a200"
                                          >
                                            Your Name
                                          </h3>
                                          <div
                                            class="
                                              font-weight-light
                                              text-h6
                                              mb-2
                                            "
                                          >
                                            Lorem Ipsum is simply dummy text of
                                            the printing and typesetting
                                            industry.
                                          </div>
                                        </v-card-text>
                                      </v-card>
                                    </v-hover>
                                  </v-col>
                                </v-row>
                              </v-container>
                            </v-tab-item>
                          </v-card>
                        </v-tabs-items>
                      </v-flex>
                    </v-layout>
                  </v-container>
                </v-fade-transition>
              </v-container>
            </v-content>
          </v-container>
        </v-container>
      </v-main>
    </v-img>

</template>
<script>
export default {
  data() {
    return {
      tab: null,
      tabnames: [
        'C',
        'Project Manager',
        'Designer',
        'Front-end',
        'Back-end',
        'Mobile Dev',
        'Quality Assurance',
        'Creative',
      ],
    }
  },
  head() {
    return {
      title: 'Members',
      overlay: false,
    }
  },
}
</script>

<style>
::selection {
  background: #ffc300;
}
</style>