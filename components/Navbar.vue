<template>
  <v-app-bar
    class="transparent elevation-0"
    app
  >
    <v-menu
      transition="slide-y-transition"
      bottom
      offset-y
    >
      <template #activator="{ on, attrs }">
        <v-btn
          class="hidden-sm-and-up"
          plain
          icon
          v-bind="attrs"
          v-on="on"
        >
          <v-icon>mdi-menu</v-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(menu, i) in menus"
          :key="i"
          dense
        >
          <v-icon class="pr-4">{{ menu.icon }}</v-icon>
          <v-list-item-title>{{ menu.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
    <v-toolbar-title class="hidden-xs-only">Svknd.id</v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items
      v-for="(menu, i) in menus"
      :key="i"
      class="hidden-xs-only"
    >
      <v-btn plain>
        <v-icon class="pr-2" small>{{ menu.icon }}</v-icon>
        {{ menu.title }}
      </v-btn>
    </v-toolbar-items>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      menus: [
        { title: 'Home', icon: 'mdi-home' },
        { title: 'Member', icon: 'mdi-account-group' },
        { title: 'Internship', icon: 'mdi-school' },
        { title: 'Join Us', icon: 'mdi-briefcase-check' },
      ],
    }
  }
}
</script>
