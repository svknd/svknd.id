<template>
  <v-container
    class="align-end pt-3 pt-lg-3 pt-sm-10"
    fill-height
  >
    <v-row
      justify="center"
      cols="auto"
    >
      <v-col cols="auto">
        <h1>Internship</h1>
      </v-col>
    </v-row>
    <v-row justify="center">
      <v-col
        v-for="(intern, i) in interns"
        :key="i"
        cols="auto"
        class="pt-0"
      >
        <v-card width="200">
          <v-img :src="intern.photo"></v-img>
          <v-card-title>{{ intern.name }}</v-card-title>
          <v-card-text>{{ intern.text }}</v-card-text>
          <v-card-actions class="justify-center flex-wrap">
            <v-btn
              v-for="(social, j) in intern.socials"
              :key="j"
              :href="social.link"
              class="ml-0 mt-1"
              target="_blank"
              plain
              small
            >
              <v-icon
                class="pr-1"
                small
              >{{ social.icon }}</v-icon>
              <span class="mt-auto">
                {{ social.name }}
              </span>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      interns: [
        {
          name: 'Placeholder',
          photo: 'https://via.placeholder.com/200x300',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
          socials: [
            {
              name: 'Linkedin',
              icon: 'mdi-linkedin',
              link: ''
            },
            {
              name: 'GitHub',
              icon: 'mdi-github',
              link: ''
            },
            {
              name: 'Instagram',
              icon: 'mdi-instagram',
              link: ''
            },
          ]
        },
        {
          name: 'Placeholder',
          photo: 'https://via.placeholder.com/200x300',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
          socials: [
            {
              name: 'Linkedin',
              icon: 'mdi-linkedin',
              link: ''
            },
            {
              name: 'GitHub',
              icon: 'mdi-github',
              link: ''
            },
            {
              name: 'Instagram',
              icon: 'mdi-instagram',
              link: ''
            },
          ]
        },
        {
          name: 'Placeholder',
          photo: 'https://via.placeholder.com/200x300',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
          socials: [
            {
              name: 'Linkedin',
              icon: 'mdi-linkedin',
              link: ''
            },
            {
              name: 'GitHub',
              icon: 'mdi-github',
              link: ''
            },
            {
              name: 'Instagram',
              icon: 'mdi-instagram',
              link: ''
            },
          ]
        },
        {
          name: 'Placeholder',
          photo: 'https://via.placeholder.com/200x300',
          text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit',
          socials: [
            {
              name: 'Linkedin',
              icon: 'mdi-linkedin',
              link: ''
            },
            {
              name: 'GitHub',
              icon: 'mdi-github',
              link: ''
            },
            {
              name: 'Instagram',
              icon: 'mdi-instagram',
              link: ''
            },
          ]
        },
      ]
    }
  },
  head() {
    return {
      title: 'Internship',
    }
  }
}
</script>
