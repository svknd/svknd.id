<template>
    <v-app-bar fixed class="navbar" height="80px">
        <img class="logo-savikindo" src="../assets/img/logo-savikindo.png" alt="">
        <v-spacer>
        </v-spacer>
        <v-list class="transparent d-none d-md-flex d-lg-flex">
        <v-btn text class="button" v-for="menu in menus" :key="menu" :href="menu.tujuan">
            {{menu.title}}
        </v-btn>
        </v-list>
        <div class="text-center navbar-hp d-flex d-sm-none">
            <v-menu offset-y>
                <template v-slot:activator="{ on, attrs }">
                    <v-btn class="btn-hp" rounded
                    dark
                    v-bind="attrs"
                    v-on="on"
                        >
                    <v-icon color="black">mdi-menu</v-icon>
                    </v-btn>
                </template>
                <v-list>
                    <v-list-item
                    v-for="(menu, i) in menus"
                    :key="i"
                    :href="menu.tujuan"
                    >
                    <v-list-item-title>{{ menu.title }}</v-list-item-title>
                    </v-list-item>
                </v-list>
            </v-menu>
        </div>
    </v-app-bar>
</template> 
    
<script>
export default {
    data() {
        return{
            menus:[
                {
                    title: "Home",
                    tujuan : "#home"
                },
                {
                    title: "Member",
                    tujuan : "#member"
                },
                {
                    title: "Internship",
                    tujuan : "#internship"
                },
                {
                    title: "Join Us",
                    tujuan : "#joinus"
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
</style>