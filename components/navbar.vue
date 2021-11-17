<template>            
  
       <v-app-bar
          fixed
          elevate-on-scroll
          class="elevation-0 d-flex justify-center"
          :class="(scrollY < 10) ? 'transparent' : 'white'">
          <v-container
          class="d-flex">   
      <v-toolbar-items>
        <v-container class="pl-sm-16">
          <a href="/"
             style="text-decoration:none;"
             class="align-left"
            :class="(scrollY < 10) ? 'white--text' : 'black--text'"
             
          >
          <h2>
               SVKND.id
          </h2>
         
          </a>
          </v-container>
      </v-toolbar-items>
    
       <v-container class="d-flex justify-end "
        style="margin-left:100px" >
    <v-toolbar-items
      v-for="(menu, i) in menus"
      :key="i"  
      class="hidden-xs-only "
    >
    
      <v-btn small
        :class="(scrollY < 10) ? 'white--text' : 'black--text'"
        text
        plain
      

      >
        {{ menu.title }}
      </v-btn>

    </v-toolbar-items>
    </v-container>
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
          fab
          v-bind="attrs"
          v-on="on"

        >
          <v-container class="d-flex mt-4"
                       style="margin-right:20px">
          <v-btn flat icon>
             <v-icon
              :class="(scrollY < 10) ? 'white--text' : 'black--text'">mdi-menu</v-icon>
          </v-btn>
          </v-container>
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(menu, i) in menus"
          :key="i"
          dense
        >
          <v-icon small class="pr-2">{{ menu.icon }}</v-icon>
          <v-list-item-title>{{ menu.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
        </v-container>
  </v-app-bar>

</template>





<script>
export default {
  data() {
    return {
      windowHeight: 0,
      scrollY: 0,
      myIcon: 'mdi-menu',
      menus: [
        { title: 'Home' , icon:'mdi-home'},
        { title: 'Member', icon:'mdi-account-group'} ,
        { title: 'Internship', icon:'mdi-cast-education'},
        { title: 'Join Us' ,icon:'mdi-link-variant'},
      ],
    }
  },
  beforeMount() {
    window.addEventListener('scroll', this.handleScroll);
    window.addEventListener('resize', this.handleHeight);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
    window.removeEventListener('resize', this.handleHeight);
  },
  mounted() {
    this.$nextTick(function () {
      this.windowHeight = window.innerHeight;
    
    });
  },
  methods: {
    handleScroll () {
      this.scrollY = window.scrollY;
    },
    handleHeight () {
      this.windowHeight = window.innerHeight;
    },
    changeIcon() {
      this.myIcon = 'home';
    }
  }
}
</script>





