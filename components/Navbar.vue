<template>
    <v-app-bar
    color="grey darken-4 white--text"
    app
    elevate-on-scroll  
    >

    <div class="pl-16">
    <v-img  src="/logo.png" alt="logo"
            max-width="150px"
            max-height="45px"
            class="pl-0"
    ></v-img>
    </div>



    <v-spacer></v-spacer>

    <div class="pr-16">
     <v-btn
        class="mr-3 fas fa-phone-square-alt"
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
