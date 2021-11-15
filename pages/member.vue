<template>
    <v-main
    class="red"
    >
    <v-row justify="center">
        <v-col cols="auto">
            <v-text class="text-h3 font-weight-light">TEAM SAVIKINDO TECH</v-text>
        </v-col>
    </v-row>

    <v-row justify="center">
        <v-col cols="auto">
            <v-text class="text-h3 font-weight-light">TEAM SAVIKINDO TECH</v-text>
        </v-col>
    </v-row>

        <div
        align = "center"
        >

        <!-- Meresponsivekan Justify menggunakan cara manual pada ukuran tablet ke bawah -->    
        <v-container
        v-for= "(part, a) in parts"
        :key= "a"
        class="mb-5 con hidden-sm-and-up"
        :style= "part.height"
        static  
        >
        <br>
        <v-row justify="center">
            <v-col cols="auto">
                <h2>{{part.title}}</h2>
            </v-col>
        </v-row>
        
        <v-row 
        class="mx-15 overflow-x-auto flex-nowrap" 
        justify= "start" 
        >
            <v-col
            v-for= "(orang, n) in part.card"
            :key= "n"
            cols="auto" 
            >
                        <v-card 
                        height="auto"
                        width="220px" 
                        class="white card"  
                        style="border:5px solid black" 
                        >
                        <v-img src="https://via.placeholder.com/120x160"></v-img>
                        <v-card-text>
                            <hr>
                                Nama : {{orang.nama}}
                            <hr>
                        </v-card-text>
                    </v-card>
                    </v-col>
                </v-row>
        </v-container>


        <!-- Meresponsivekan Justify menggunakan cara manual pada ukuran laptop -->
        <v-container
        v-for= "(part, a) in parts"
        :key= "a"
        class="mb-5 con hidden-xs-only"
        :style= "part.height"
        static  
        >
        <br>
        <v-row justify="center">
            <v-col cols="auto">
                <h2>{{part.title}}</h2>
            </v-col>
        </v-row>
        
        <v-row 
        class="mx-15 overflow-x-auto flex-nowrap" 
        :justify= "(part.card.length < 5) ? 'center' : 'start'" 
        >
            <v-col
            v-for= "(orang, n) in part.card"
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
                            <hr>
                                Nama : {{orang.nama}}
                            <hr>
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
                card : [
                    {
                        nama : 'Ucup'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                ],
                justify : 'start',
                height : 'height:520px'
            },
            {
                warna : 'red',
                title : 'Backend',
                card : [
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                ],
                justify : 'center',
                height : 'height:510px'
            },
            {
                warna : 'green',
                title : 'Frond end',
                card : [
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                ],
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