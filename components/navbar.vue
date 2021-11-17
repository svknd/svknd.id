<template>
  <v-app-bar
    fixed
    elevate-on-scroll
    class="elevation-3 d-flex justify-center"
    :class="scrollY < 10 ? 'transparent' : 'white'"
  >
    <v-container class="d-flex">
      <v-toolbar-items>
        <v-container>
          <a
            href="/"
            style="text-decoration: none"
            class="align-left"
            :class="scrollY < 10 ? 'white--text' : 'black--text'"
          >
            <h2>SVKND.id</h2>
          </a>
        </v-container>
      </v-toolbar-items>

      <v-container class="d-flex justify-end" style="margin-left: 120px">
        <v-toolbar-items
          v-for="(menu, key) in menus"
          :key="key"
          class="hidden-xs-only"
        >
          <v-btn
            small
            :class="scrollY < 10 ? 'white--text' : 'black--text'"
            text
            plain
            :href="menu.link"
          >
            {{ menu.title }}
          </v-btn>
        </v-toolbar-items>

        <!--JOIN US DIALOG STAARRRRRTTT -->
        <v-toolbar-items>
          <v-dialog transition="dialog-bottom-transition" fullscreen>
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                class="hidden-xs-only"
                v-bind="attrs"
                v-on="on"
                small
                text
                plain
                :class="scrollY < 10 ? 'white--text' : 'black--text'"
              >
                Join Us
              </v-btn>
            </template>

            <template v-slot:default="dialog">
              <v-card pr-0>
                <v-container fluid fill-height>
                  <v-row class="overflow-hidden">
                    <v-col
                      cols="3"
                      style="background-color: #ffc72e; height: 100vh"
                      absolute
                      class="pa-0 pt-9 d-none d-lg-flex d-md-none"
                    >
                      <v-container class="px-9">
                        <h2 class="text-h5 text-left font-weight-bold">
                          Get in touch
                        </h2>
                        <br />
                        <v-text class="text-body 2 font-weight-light"
                          >We are always here, Our friendly team always here to
                          chat!</v-text
                        >
                        <br />
                        <br />
                        <div class="d-flex">
                          <v-icon>mdi-email-outline</v-icon>
                          <v-text class="ml-2">
                            <h3 class="text-body font-weight-medium">
                              Chat to us
                            </h3>
                          </v-text>
                        </div>

                        <h5 class="text-caption mt-1" style="margin-left: 33px">
                          Our friendly team is here to help
                        </h5>
                        <a
                          href="mailto:info@savikindo.co.id"
                          class="text-decoration-none"
                          style="color: black"
                          ><h5
                            class="text-body mt-1 font-weight-medium"
                            style="margin-left: 33px"
                          >
                            info@savikindo.co.id
                          </h5></a
                        >
                        <br />
                        <div class="d-flex">
                          <v-icon class="">mdi-map</v-icon>
                          <v-text class="ml-2">
                            <h3 class="text-body 1 font-weight-medium">
                              Office
                            </h3>
                          </v-text>
                        </div>

                        <h5 class="text-caption mt-1" style="margin-left: 33px">
                          Come and say hello!
                        </h5>
                        <a
                          href="https://www.google.com/maps/search/Jl.+Kanayakan+Lama+No.40,+Dago,+Kecamatan+Coblong,+Kota+Bandung,+Jawa+Barat+40135/@-6.8764856,107.6197112,20.12z"
                          class="text-decoration-none"
                          style="color: black"
                          target="blank"
                          ><h5
                            class="text-body mt-1 font-weight-medium"
                            style="margin-left: 33px"
                          >
                            Jl. Kanayakan Lama No.40, Dago, Kecamatan Coblong,
                            Kota Bandung, Jawa Barat 40135
                          </h5></a
                        >

                        <br />
                        <div class="d-flex">
                          <v-icon class="">mdi-phone-outline</v-icon>
                          <v-text class="ml-2">
                            <h3 class="text-body 1 font-weight-medium">
                              Phone
                            </h3>
                          </v-text>
                        </div>

                        <h5 class="text-caption mt-1" style="margin-left: 33px">
                          Monday - Friday | 09.00 PM - 17.00
                        </h5>
                        <a
                          href="tel://02220278381"
                          class="text-decoration-none"
                          style="color: black"
                          ><h5
                            class="text-body mt-1 font-weight-medium"
                            style="margin-left: 33px"
                          >
                            (022) 2027 8381
                          </h5></a
                        >
                      </v-container>
                    </v-col>
                    <v-btn
                      icon
                      dark
                      @click="dialog.value = false"
                      :order="$vuetify.breakpoint.xsAndUp ? 'first' : 'end'"
                    >
                      <v-icon color="black">mdi-close</v-icon>
                    </v-btn>
                    <v-col
                      align="center"
                      class="d-flex align-center justify-center"
                    >
                      <v-card
                        v-scroll.self="onScroll"
                        class="overflow-y-auto"
                        max-height="85vh"
                        width="905px"
                        align="left"
                      >
                        <h1 class="pb-0 pt-3 pl-5">Let's Collaborate!</h1>
                        <h3 class="pl-5 pb-2 font-weight-medium">
                          You can reach us anytime via
                          <a
                            href="mailto:info@savikindo.co.id"
                            style="color: #ffc72e"
                            class="text-decoration-none"
                            >info@savikindo.co.id</a
                          >
                        </h3>
                        <v-stepper v-model="e6" vertical>
                          <v-stepper-step
                            color="#FE9720"
                            :complete="e6 > 1"
                            step="1"
                          >
                            Profile
                          </v-stepper-step>

                          <v-stepper-content step="1">
                            <!-- CONTENT NO 1 -->
                            <v-card flat>
                              <v-snackbar
                                v-model="snackbar"
                                absolute
                                top
                                right
                                color="success"
                              >
                                <v-icon dark>
                                  mdi-checkbox-marked-circle
                                </v-icon>
                              </v-snackbar>
                              <v-form ref="form" @submit.prevent="submit">
                                <v-container fluid>
                                  <v-row>
                                    <v-col cols="12" sm="6">
                                      <v-text-field
                                        v-model="form.first"
                                        :rules="rules.name"
                                        color="purple darken-2"
                                        label="First name"
                                        required
                                      ></v-text-field>
                                    </v-col>

                                    <v-col cols="12" sm="6">
                                      <v-text-field
                                        v-model="form.last"
                                        :rules="rules.name"
                                        color="blue darken-2"
                                        label="Last name"
                                        required
                                      ></v-text-field>
                                    </v-col>
                                    <v-col cols="12" sm="16">
                                      <v-text-field
                                        v-model="form.email"
                                        :rules="rules.email"
                                        color="blue darken-2"
                                        label="Email"
                                        required
                                      ></v-text-field>
                                    </v-col>
                                    <v-col cols="12">
                                      <v-textarea
                                        v-model="form.address"
                                        color="teal"
                                        required
                                        :rules="rules.address"
                                      >
                                        <template v-slot:label>
                                          <div>Address</div>
                                        </template>
                                      </v-textarea>
                                    </v-col>
                                  </v-row>
                                </v-container>
                                <v-card-actions> </v-card-actions>
                              </v-form>
                              <v-dialog v-model="terms" width="70%">
                                <v-card>
                                  <v-card-title class="text-h6">
                                    Terms
                                  </v-card-title>
                                  <v-card-text v-for="n in 5" :key="n">
                                    {{ content }}
                                  </v-card-text>
                                  <v-card-actions>
                                    <v-spacer></v-spacer>
                                    <v-btn
                                      text
                                      color="purple"
                                      @click="terms = false"
                                    >
                                      Ok
                                    </v-btn>
                                  </v-card-actions>
                                </v-card>
                              </v-dialog>
                              <v-dialog v-model="conditions" width="70%">
                                <v-card>
                                  <v-card-title class="text-h6">
                                    Conditions
                                  </v-card-title>
                                  <v-card-text v-for="n in 5" :key="n">
                                    {{ content }}
                                  </v-card-text>
                                  <v-card-actions>
                                    <v-spacer></v-spacer>
                                    <v-btn
                                      text
                                      color="purple"
                                      @click="conditions = false"
                                    >
                                      Ok
                                    </v-btn>
                                  </v-card-actions>
                                </v-card>
                              </v-dialog>
                            </v-card>

                            <v-btn color="primary" @click="e6 = 2">
                              Continue
                            </v-btn>
                            <v-btn text> Cancel </v-btn>
                          </v-stepper-content>

                          <v-stepper-step
                            color="#FE9720"
                            :complete="e6 > 2"
                            step="2"
                          >
                            Experience
                          </v-stepper-step>

                          <v-stepper-content step="2">
                            <v-col cols="12">
                              <v-textarea
                                v-model="form.experience"
                                color="teal"
                                required
                                :rules="rules.experience"
                              >
                                <template v-slot:label>
                                  <div>Your Experience</div>
                                </template>
                              </v-textarea>
                            </v-col>
                            <v-col cols="12" sm="5">
                              <v-file-input
                                show-size
                                label="Your Portfolio (Optional) "
                              ></v-file-input>
                            </v-col>
                            <v-btn color="primary" @click="e6 = 3">
                              Continue
                            </v-btn>
                            <v-btn text> Cancel </v-btn>
                          </v-stepper-content>

                          <v-stepper-step
                            color="#FE9720"
                            :complete="e6 > 3"
                            step="3"
                          >
                            Skills
                          </v-stepper-step>

                          <v-stepper-content step="3">
                            <v-layout
                              row
                              class="pa-4 pl-6 pb-1 pa-1-sm pl-16sm"
                            >
                              <v-flex
                                v-for="(category, index) in types"
                                :key="types[index].text"
                                sm6
                              >
                                <v-checkbox
                                  light
                                  :label="category.text"
                                  v-model="category.selected"
                                >
                                </v-checkbox>
                              </v-flex>
                            </v-layout>
                            <v-row align="center" class="ml-3 mt-0 mb-6">
                              <v-checkbox
                                v-model="enabled"
                                hide-details
                                class="shrink mr-1 mt-0"
                              ></v-checkbox>
                              <v-text-field
                                :disabled="!enabled"
                                label="Other"
                                class=""
                              ></v-text-field>
                            </v-row>
                            <v-btn color="primary" @click="e6 = 1">
                              Send
                            </v-btn>
                            <v-btn text> Cancel </v-btn>
                          </v-stepper-content>
                        </v-stepper>
                      </v-card>
                    </v-col>
                  </v-row>
                </v-container>
              </v-card>
            </template>
          </v-dialog>
        </v-toolbar-items>
      </v-container>
      <!-- JOIN US DIALOG END -->

      <v-menu transition="slide-y-transition" bottom offset-y>
        <template #activator="{ on, attrs }">
          <v-btn
            class="hidden-sm-and-up"
            plain
            icon
            fab
            v-bind="attrs"
            v-on="on"
          >
            <v-container class="d-flex mt-4" style="margin-right: 20px">
              <v-btn flat icon>
                <v-icon :class="scrollY < 10 ? 'white--text' : 'black--text'"
                  >mdi-menu</v-icon
                >
              </v-btn>
            </v-container>
          </v-btn>
        </template>
        <v-list>
          <v-list-item v-for="(menu, i) in menus" :key="i" dense>
            <v-btn plain small style="padding: 1px" :href="menu.link">
              <v-icon small class="pr-2">{{ menu.icon }}</v-icon>
              <v-list-item-title align="center" class="text-left"
                >{{ menu.title }}
              </v-list-item-title>
            </v-btn>
          </v-list-item>
          <v-toolbar-items>
            <v-dialog
              fullscreen
              transition="dialog-bottom-transition"
              max-width="600"
            >
              <template v-slot:activator="{ on, attrs }">
                <v-btn
                  v-bind="attrs"
                  v-on="on"
                  text
                  plain
                  style="
                    margin-left: 18px;
                    padding-top: 8px;
                    padding-bottom: 10px;
                    padding-left: 0px;
                  "
                >
                  <v-icon small class="pr-2">mdi-account-arrow-left</v-icon>
                  JOIN US
                </v-btn>
              </template>

              <template v-slot:default="dialog">
              <v-card pr-0>
                <v-container fluid fill-height>
                  <v-row class="overflow-hidden">
                    <v-col
                      cols="3"
                      style="background-color: #ffc72e; height: 100vh"
                      absolute
                      class="pa-0 pt-9 d-none d-lg-flex d-md-none"
                    >
                      <v-container class="px-9">
                        <h2 class="text-h5 text-left font-weight-bold">
                          Get in touch
                        </h2>
                        <br />
                        <v-text class="text-body 2 font-weight-light"
                          >We are always here, Our friendly team always here to
                          chat!</v-text
                        >
                        <br />
                        <br />
                        <div class="d-flex">
                          <v-icon class="">mdi-email-outline</v-icon>
                          <v-text class="ml-2">
                            <h3 class="text-body 1 font-weight-medium">
                              Chat to us
                            </h3>
                          </v-text>
                        </div>

                        <h5 class="text-caption mt-1" style="margin-left: 33px">
                          Our friendly team is here to help
                        </h5>
                        <a
                          href="mailto:info@savikindo.co.id"
                          class="text-decoration-none"
                          style="color: black"
                          ><h5
                            class="text-body mt-1 font-weight-medium"
                            style="margin-left: 33px"
                          >
                            info@savikindo.co.id
                          </h5></a
                        >
                        <br />
                        <div class="d-flex">
                          <v-icon class="">mdi-map</v-icon>
                          <v-text class="ml-2">
                            <h3 class="text-body 1 font-weight-medium">
                              Office
                            </h3>
                          </v-text>
                        </div>

                        <h5 class="text-caption mt-1" style="margin-left: 33px">
                          Come and say hello!
                        </h5>
                        <a
                          href="https://www.google.com/maps/search/Jl.+Kanayakan+Lama+No.40,+Dago,+Kecamatan+Coblong,+Kota+Bandung,+Jawa+Barat+40135/@-6.8764856,107.6197112,20.12z"
                          class="text-decoration-none"
                          style="color: black"
                          target="blank"
                          ><h5
                            class="text-body mt-1 font-weight-medium"
                            style="margin-left: 33px"
                          >
                            Jl. Kanayakan Lama No.40, Dago, Kecamatan Coblong,
                            Kota Bandung, Jawa Barat 40135
                          </h5></a
                        >

                        <br />
                        <div class="d-flex">
                          <v-icon class="">mdi-phone-outline</v-icon>
                          <v-text class="ml-2">
                            <h3 class="text-body 1 font-weight-medium">
                              Phone
                            </h3>
                          </v-text>
                        </div>

                        <h5 class="text-caption mt-1" style="margin-left: 33px">
                          Monday - Friday | 09.00 PM - 17.00
                        </h5>
                        <a
                          href="tel://02220278381"
                          class="text-decoration-none"
                          style="color: black"
                          ><h5
                            class="text-body mt-1 font-weight-medium"
                            style="margin-left: 33px"
                          >
                            (022) 2027 8381
                          </h5></a
                        >
                      </v-container>
                    </v-col>
                    <v-btn
                      icon
                      dark
                      @click="dialog.value = false"
                      :order="$vuetify.breakpoint.xsAndUp ? 'first' : 'end'"
                    >
                      <v-icon color="black">mdi-close</v-icon>
                    </v-btn>
                    <v-col
                      align="center"
                      class="d-flex align-center justify-center"
                    >
                      <v-card
                        v-scroll.self="onScroll"
                        class="overflow-y-auto"
                        max-height="85vh"
                        width="905px"
                        align="left"
                      >
                        <h1 class="pb-0 pt-3 pl-5">Let's Collaborate!</h1>
                        <h3 class="pl-5 pb-2 font-weight-medium">
                          You can reach us anytime via
                          <a
                            href="mailto:info@savikindo.co.id"
                            style="color: #ffc72e"
                            class="text-decoration-none"
                            >info@savikindo.co.id</a
                          >
                        </h3>
                        <v-stepper v-model="e6" vertical>
                          <v-stepper-step
                            color="#FE9720"
                            :complete="e6 > 1"
                            step="1"
                          >
                            Profile
                          </v-stepper-step>

                          <v-stepper-content step="1">
                            <!-- CONTENT NO 1 -->
                            <v-card flat>
                              <v-snackbar
                                v-model="snackbar"
                                absolute
                                top
                                right
                                color="success"
                              >
                                <v-icon dark>
                                  mdi-checkbox-marked-circle
                                </v-icon>
                              </v-snackbar>
                              <v-form ref="form" @submit.prevent="submit">
                                <v-container fluid>
                                  <v-row>
                                    <v-col cols="12" sm="6">
                                      <v-text-field
                                        v-model="form.first"
                                        :rules="rules.name"
                                        color="purple darken-2"
                                        label="First name"
                                        required
                                      ></v-text-field>
                                    </v-col>

                                    <v-col cols="12" sm="6">
                                      <v-text-field
                                        v-model="form.last"
                                        :rules="rules.name"
                                        color="blue darken-2"
                                        label="Last name"
                                        required
                                      ></v-text-field>
                                    </v-col>
                                    <v-col cols="12" sm="16">
                                      <v-text-field
                                        v-model="form.email"
                                        :rules="rules.email"
                                        color="blue darken-2"
                                        label="Email"
                                        required
                                      ></v-text-field>
                                    </v-col>
                                    <v-col cols="12">
                                      <v-textarea
                                        v-model="form.address"
                                        color="teal"
                                        required
                                        :rules="rules.address"
                                      >
                                        <template v-slot:label>
                                          <div>Address</div>
                                        </template>
                                      </v-textarea>
                                    </v-col>
                                  </v-row>
                                </v-container>
                                <v-card-actions> </v-card-actions>
                              </v-form>
                              <v-dialog v-model="terms" width="70%">
                                <v-card>
                                  <v-card-title class="text-h6">
                                    Terms
                                  </v-card-title>
                                  <v-card-text v-for="n in 5" :key="n">
                                    {{ content }}
                                  </v-card-text>
                                  <v-card-actions>
                                    <v-spacer></v-spacer>
                                    <v-btn
                                      text
                                      color="purple"
                                      @click="terms = false"
                                    >
                                      Ok
                                    </v-btn>
                                  </v-card-actions>
                                </v-card>
                              </v-dialog>
                              <v-dialog v-model="conditions" width="70%">
                                <v-card>
                                  <v-card-title class="text-h6">
                                    Conditions
                                  </v-card-title>
                                  <v-card-text v-for="n in 5" :key="n">
                                    {{ content }}
                                  </v-card-text>
                                  <v-card-actions>
                                    <v-spacer></v-spacer>
                                    <v-btn
                                      text
                                      color="purple"
                                      @click="conditions = false"
                                    >
                                      Ok
                                    </v-btn>
                                  </v-card-actions>
                                </v-card>
                              </v-dialog>
                            </v-card>

                            <v-btn color="primary" @click="e6 = 2">
                              Continue
                            </v-btn>
                            <v-btn text> Cancel </v-btn>
                          </v-stepper-content>

                          <v-stepper-step
                            color="#FE9720"
                            :complete="e6 > 2"
                            step="2"
                          >
                            Experience
                          </v-stepper-step>

                          <v-stepper-content step="2">
                            <v-col cols="12">
                              <v-textarea
                                v-model="form.experience"
                                color="teal"
                                required
                                :rules="rules.experience"
                              >
                                <template v-slot:label>
                                  <div>Your Experience</div>
                                </template>
                              </v-textarea>
                            </v-col>
                            <v-col cols="12" sm="5">
                              <v-file-input
                                show-size
                                label="Your Portfolio (Optional) "
                              ></v-file-input>
                            </v-col>
                            <v-btn color="primary" @click="e6 = 3">
                              Continue
                            </v-btn>
                            <v-btn text> Cancel </v-btn>
                          </v-stepper-content>

                          <v-stepper-step
                            color="#FE9720"
                            :complete="e6 > 3"
                            step="3"
                          >
                            Skills
                          </v-stepper-step>

                          <v-stepper-content step="3">
                            <v-layout
                              row
                              class="pa-4 pl-6 pb-1 pa-1-sm pl-16sm"
                            >
                              <v-flex
                                v-for="(category, index) in types"
                                :key="types[index].text"
                                sm6
                              >
                                <v-checkbox
                                  light
                                  :label="category.text"
                                  v-model="category.selected"
                                >
                                </v-checkbox>
                              </v-flex>
                            </v-layout>
                            <v-row align="center" class="ml-3 mt-0 mb-6">
                              <v-checkbox
                                v-model="enabled"
                                hide-details
                                class="shrink mr-1 mt-0"
                              ></v-checkbox>
                              <v-text-field
                                :disabled="!enabled"
                                label="Other"
                                class=""
                              ></v-text-field>
                            </v-row>
                            <v-btn color="primary" @click="e6 = 1">
                              Send
                            </v-btn>
                            <v-btn text> Cancel </v-btn>
                          </v-stepper-content>
                        </v-stepper>
                      </v-card>
                    </v-col>
                  </v-row>
                </v-container>
              </v-card>
            </template>
            </v-dialog>
          </v-toolbar-items>
        </v-list>
      </v-menu>
    </v-container>
  </v-app-bar>
</template>





<script>
export default {
  data() {
    const defaultForm = Object.freeze({
      first: '',
      last: '',
      email: '',
      address: '',
      experience: '',
      Yourskills: '',
      terms: false,
    })
    return {
      enabled: false,
      windowHeight: 0,
      scrollY: 0,
      myIcon: 'mdi-menu',
      menus: [
        { title: 'Home', icon: 'mdi-home', link: '/' },
        { title: 'Member', icon: 'mdi-account-group', link: '/member' },
        {
          title: 'Internship',
          icon: 'mdi-cast-education',
          link: '/internship',
        },
      ],
      e6: 1,
      form: Object.assign({}, defaultForm),
      rules: {
        experience: [
          (val) => (val || '').length > 0 || 'This field is required',
        ],
        address: [(val) => (val || '').length > 0 || 'This field is required'],
        skills: [(val) => (val || '').length > 0 || 'This field is required'],
        email: [(val) => (val || '').length > 0 || 'This field is required'],
        name: [(val) => (val || '').length > 0 || 'This field is required'],
      },

      conditions: false,
      content:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer nec odio. Praesent libero. Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet. Duis sagittis ipsum. Praesent mauris. Fusce nec tellus sed augue semper porta. Mauris massa. Vestibulum lacinia arcu eget nulla. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Curabitur sodales ligula in libero. Sed dignissim lacinia nunc.',
      snackbar: false,
      terms: false,
      defaultForm,
      checkbox: false,

      types: [
        {
          text: 'Front-End Developer',
          value: 'Front-End Developer',
          selected: false,
        },
        {
          text: 'Back-End Developer',
          value: 'Back-End Developer',
          selected: false,
        },
        { text: 'Project Manager', value: 'Project Manager', selected: false },
        { text: 'Team Creative', value: 'Team Creative', selected: false },
        {
          text: 'Quality Assurance',
          value: 'Quality Assurance',
          selected: false,
        },
        { text: 'UI/UX Designer', value: 'UI/UX Designer', selected: false },
      ],
    }
  },

  beforeMount() {
    window.addEventListener('scroll', this.handleScroll)
    window.addEventListener('resize', this.handleHeight)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
    window.removeEventListener('resize', this.handleHeight)
  },
  mounted() {
    this.$nextTick(function () {
      this.windowHeight = window.innerHeight
    })
  },
  methods: {
    handleScroll() {
      this.scrollY = window.scrollY
    },
    onScroll() {
      this.scrollInvoked++
    },
    handleHeight() {
      this.windowHeight = window.innerHeight
    },
    changeIcon() {
      this.myIcon = 'home'
    },

    checkLength(index) {
      if (index < this.types.length - 1) {
        index = index + 1
        return index
      }
    },
  },
}
</script>

<style>
::selection {
  background: #ffc300;
}
</style>



