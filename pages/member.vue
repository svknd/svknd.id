<template>
    <v-main>
        <div
        align = "center"
        >
        <v-container
        v-for= "(part, a) in parts"
        :key= "a"
        class="mb-5 con"
        :style= "part.height"
        static  
        >
        <br>
        <v-row justify="center">
            <v-col cols="auto">
                <h2>{{part.title}}</h2>
            </v-col>
        </v-row>
        <v-row class="mx-15 overflow-x-auto flex-nowrap" justify= "start">
            <v-col
            v-for= "n in part.card"
            :key= "n"
            cols="auto" 
            >
                <v-card 
                height="auto"
                width="220px" 
                class="white card"   
                >
                    <v-img src="https://via.placeholder.com/120x160"></v-img>
                    <v-card-text>
                            {{part.nama}}
                    </v-card-text>
                </v-card>

            </v-col>
        </v-row>
        </v-container>
        </div>
    </v-main>
</template>

<script>
export default {
    data() {
        return {
        parts : [
            {
                warna : 'blue-grey darken-1',
                title : 'Bagian Administrasi',
                nama : 'Ini Nama',
                card : 6,
                justify : 'start',
                height : 'height:520px'
            },
            {
                warna : 'red',
                title : 'Backend',
                nama : 'Ini Nama',
                card : 3,
                justify : 'center',
                height : 'height:510px'
            },
            {
                warna : 'green',
                title : 'Frond end',
                nama : 'Ini Nama',
                card : 2,
                justify : 'center',
                height : 'height:510px'
            },

        ]
        }
    },
}
</script>

<style scoped>
.con {
    background-image: linear-gradient(to bottom right, rgb(5, 233, 165) , green, red);
    border: 5px solid black;
    border-radius: 20px;
}

.card {
    border-top-left-radius : 5px; 
    border-bottom-left-radius : 5px; 
}

.scroll {
    overflow-x: auto !important;
}

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px rgb(0, 38, 255); 
  border-radius: 5px;
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: rgb(153, 99, 0); 
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #008d4b; 
}
</style>