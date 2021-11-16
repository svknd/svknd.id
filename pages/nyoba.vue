<!-- Vue Template HTML Markup -->

<template>
  <!-- <v-menu>
      <template v-slot:activator= "{on, attr}">
          <v-btn
          v-bind="attr"
          v-on= "on"
          >
        Click me
        </v-btn>
      </template>

    <v-list>
      <v-list-item @click="method">
        <v-list-item-title>Option 1</v-list-item-title>
      </v-list-item>

      <v-list-item disabled>
        <v-list-item-title>Option 2</v-list-item-title>
      </v-list-item>

      <v-list-item @click="method">
        <v-list-item-title>Option 3</v-list-item-title>
      </v-list-item>
    </v-list>

  </v-menu> -->
<v-container>
  <button
  aria-expanded="false"
  aria-haspopup="true"
  role="button"
  type="button"
>
  Click me
</button>
</v-container>

</template>