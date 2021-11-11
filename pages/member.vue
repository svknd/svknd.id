<template>
    <v-app class="black px-5">
        <v-container
        static 
        v-for= "(part, n) in parts"
        :key= "n"
        :class= "part.warna "
        class="ma-5 "
        style="height:500px; width:auto"
        fluid
        >
        <br>
        <v-row justify="center">
            <v-col cols="auto">
                <h2>{{part.title}}</h2>
            </v-col>
        </v-row>
        <v-row class="mx-10 overflow-x-auto flex-nowrap" :justify= "part.justify">
            <v-col
            v-for= "n in part.card"
            :key= "n"
            cols="auto" 
            >
                <v-card 
                height="375px" 
                width="220px"    
                >
                    <v-img src="https://via.placeholder.com/120x160"></v-img>
                </v-card>

            </v-col>
        </v-row>
        </v-container>
    </v-app>
</template>

<script>
export default {
    data() {
        return {
        parts : [
            {
                warna : 'blue-grey darken-1',
                title : 'Bagian Administrasi',
                orang : [
                    {
                        nama : 'a',
                        alamat : 'anu'
                     },
                    {
                        nama : 'b',
                        alamat : 'aasdnu'
                    },
                ],
                card : 6,
                justify : 'start'
            },
            {
                warna : 'red',
                title : 'Backend',
                card : 3,
                justify : 'center'
            },
            {
                warna : 'green',
                title : 'Frond end',
                card : 2,
                justify : 'center'
            },

        ]
        }
    },
}
</script>

<style scoped>
.scroll {
    overflow-y: auto !important;
}
</style>