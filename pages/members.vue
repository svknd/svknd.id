<template>
  <main
    :class="teams[0].background"
    class="pt-0 pt-lg-1 pt-sm-8"
  >
    <v-container
      v-for="(team, i) in teams"
      :key="i"
      :class="team.background"
      class="px-10 py-6"
      fill-height
      fluid
    >
      <v-row
        justify="center"
        cols="auto"
      >
        <h1 class="text-center">
          {{ team.role }}
        </h1>
      </v-row>
      <v-row justify="center">
        <v-col
          v-for="(member, j) in team.members"
          :key="j"
          class="flex-grow-0"
        >
          <v-hover v-slot="{ hover }">
            <v-card
              class="mx-auto"
              :max-width="hover ? 200 : 150"
            >
              <v-img
                class="white--text align-end"
                :src="member.photo"
              >
                <v-card-title
                  class="d-block"
                  style="word-break: normal"
                  :class="hover ? '' : 'text-truncate'"
                >
                  {{ member.name }}
                </v-card-title>
              </v-img>
            </v-card>
          </v-hover>
        </v-col>
      </v-row>
    </v-container>
  </main>
</template>

<script>
export default {
  data() {
    return {
      teams: [
        {
          role: 'CEO',
          background: 'green lighten-3',
          members: [
            {
              name: 'Placeholder',
              photo: 'https://via.placeholder.com/200x300'
            }
          ]
        },
        {
          role: 'Frontend Engineer',
          background: 'blue lighten-3',
          members: [
            {
              name: 'Placeholder Placeholder Placeholder',
              photo: 'https://via.placeholder.com/200x300'
            },
            {
              name: 'Placeholder',
              photo: 'https://via.placeholder.com/200x300'
            },
          ]
        },
        {
          role: 'Backend Engineer',
          background: 'indigo lighten-2',
          members: [
            {
              name: 'Placeholder',
              photo: 'https://via.placeholder.com/200x300'
            },
            {
              name: 'Placeholder',
              photo: 'https://via.placeholder.com/200x300'
            },
            {
              name: 'Placeholder',
              photo: 'https://via.placeholder.com/200x300'
            },
          ]
        },
      ]
    }
  },
  head() {
    return {
      title: 'Members',
    }
  }
}
</script>

<style>
.v-card {
  transition: all 0.3s;
}
</style>
