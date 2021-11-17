<template>
    <v-app-bar
    color="grey darken-4 white--text"
    app
    elevate-on-scroll  
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
          <v-icon color="white">mdi-menu</v-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(menu, i) in menus"
          :key="i"
          :href="menu.link"
          dense
        >
          <!-- <v-list-item-icon>
            <v-icon>{{ menu.icon }}</v-icon>
          </v-list-item-icon> -->
          <v-list-item-title>{{ menu.item }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>

    <div class="mx-auto">
    <v-img  src="/logo.png" alt="logo"
            max-width="150px"
            max-height="45px"
            class="pl-0"
    ></v-img>
    </div>



    <v-spacer></v-spacer>

    <div class="pr-16 hidden-xs-only">
     <v-btn
        class="mr-lg-3  fas fa-phone-square-alt"
        :disabled="loading"
        color="white"
        plain
        v-for= "(menu, a) in menus"
        :key= "a"
        :href= "menu.link"
        style="padding:10px"
      >{{ menu.item }}</v-btn>
    </div>

    </v-app-bar>
</template>

<style scoped>
.font{
    font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}
</style>

<script>
export default {
    data(){
        return {
            menus : [
                {item : 'Homepage', link : '/'},
                {item : 'Member', link : '/member'},
                {item : 'Internship', link : '/internship'},
                {item : 'Join Us', link : '/joinus'}
            ],
        }
    },
    computed : {
      links() {
       return  this.menus.map((item, index)=>({id:index,...item}))
        }
    },
}
</script>