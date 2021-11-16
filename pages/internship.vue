<template>
    <v-main class="cyan accent-2">
        <div
        align = "center"
        >

        <!-- Meresponsivekan Justify menggunakan cara manual pada ukuran tablet ke bawah -->
        <v-container
        v-for= "(part, a) in parts"
        :key= "a"
        class="mb-5 con hidden-sm-and-up teal darken-3 mb-16"
        :style= "part.height"
        static  
        >
        <br>
        <v-row justify="center">
            <v-col cols="auto">
                <v-text class="text-h5 font-weight-bold white--text">Internship</v-text>
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
                <v-hover v-slot= "{ hover }">
                        <v-card 
                        height="auto"
                        width="220px" 
                        class="white card"
                        :elevation="hover ? 20 : 2"
                        :class="{ 'on-hover': hover }"   
                        >
                        <v-img src="https://via.placeholder.com/120x160"></v-img>
                        <v-card-text>
                                {{orang.nama}}
                                <hr>
                                {{orang.instansi}}
                        </v-card-text>
                    </v-card>
                </v-hover>
                    </v-col>
                </v-row>
        </v-container>

        <!-- Meresponsivekan Justify menggunakan cara manual pada ukuran laptop -->
        <v-container
        v-for= "(part, a) in parts"
        :key= "a"
        class="mb-5 con hidden-xs-only teal darken-3 mb-16"
        :style= "part.height"
        static  
        >
        <br>
        <v-row justify="center">
            <v-col cols="auto">
                <v-text class="text-h5 font-weight-bold white--text">Internship</v-text>
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
                <v-hover v-slot= "{ hover }">
                        <v-card 
                        height="auto"
                        width="220px" 
                        class="white card"   
                        :elevation="hover ? 20 : 2"
                        :class="{ 'on-hover': hover }" 
                        >
                        <v-img src="https://via.placeholder.com/120x160"></v-img>
                        <v-card-text>
                                {{orang.nama}}
                                <hr>
                                {{orang.instansi}}
                        </v-card-text>
                    </v-card>
                </v-hover>
                    </v-col>
                </v-row>
                <br>
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
                card : [
                    {
                        nama : 'Ucup',
                        instansi : 'SMKN 13 Bandung'
                    },
                    {
                        nama : 'Fadhil Maulana',
                        instansi : 'SMKN 13 Bandung'
                    },
                    {
                        nama : 'Fadhil Maulana',
                        instansi : 'SMKN 13 Bandung'
                    },
                    {
                        nama : 'Ucup',
                        instansi : 'SMKN 13 Bandung'
                    },
                    {
                        nama : 'Fadhil Maulana',
                        instansi : 'SMKN 13 Bandung'
                    },
                    {
                        nama : 'Fadhil Maulana',
                        instansi : 'SMKN 13 Bandung'
                    },
                ],
            },
            
        ]
        }
    },
}
</script>

<style scoped>
.con {
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