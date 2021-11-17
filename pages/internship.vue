<template>
<v-container>
    <v-row justify="center">
        <v-col cols="auto">
            <v-text class="text-h4 font-weight-bold title1">INTERNSHIP</v-text>
        </v-col>
    </v-row>

    <v-row>
   <v-container class="black">
        <div
        align = "center"
        fluid   
        >

        <!-- Meresponsivekan Justify menggunakan cara manual pada ukuran tablet ke bawah -->
        <v-container
        v-for= "(part, a) in parts"
        :key= "a"
        class="mb-5 con hidden-sm-and-up con1"
        fluid
        >
        <v-row 
        class="mx-15 overflow-x-auto flex-nowrap" 
        justify= "start"
        fill-height 
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
        class="mb-5 con hidden-xs-only con1"
        fluid
        >
        <v-row 
        class="mx-15 overflow-x-auto flex-nowrap" 
        :justify= "(part.card.length < 5) ? 'center' : 'start'"
        fill-height
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
        <br><br>
    </v-container>
</v-row>
</v-container>
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
.title1 {
    color: rgb(0, 102, 77);  
}

.con {
    border: 5px solid black;
    border-radius: 20px;
}

.con1 {
    background-color: #3F3D56;
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