<template>
    <v-main
    class="teal darken-2"
    >
    <v-container class="mb-3">
    <v-row justify="center hidden-sm-and-up text-decoration-underline">
        <v-col cols="auto">
            <v-text class="text-h5 font-weight-bold text-decoration-underline">TEAM SAVIKINDO TECH</v-text>
        </v-col>
    </v-row>

    <v-row justify="center hidden-md-and-up hidden-xs-only text-decoration-underline">
        <v-col cols="auto">
            <v-text class="text-h4 font-weight-bold text-decoration-underline">TEAM SAVIKINDO TECH</v-text>
        </v-col>
    </v-row>

    <v-row justify="center hidden-sm-and-down">
        <v-col cols="auto">
            <v-text class="text-h2 font-weight-bold text-decoration-underline">TEAM SAVIKINDO TECH</v-text>
        </v-col>
    </v-row>
    </v-container>

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
        style="border:5px solid black" 
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
                        style="border:5px solid black" 
                        :elevation="hover ? 20 : 2"
                        :class="{ 'on-hover': hover }" 
                        >
                        <v-img src="https://via.placeholder.com/120x160"></v-img>
                        <v-card-text>
                           <hr>
                            {{orang.nama}}
                            <hr>
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
        class="mb-5 con hidden-xs-only"
        :style= "part.height"
        static  
        >
        <br>
        <v-row justify="center">
            <v-col cols="auto">
                <v-text class="text-h5 font-weight-bold">{{part.title}}</v-text>
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
                            <hr>
                            {{orang.nama}}
                            <hr>
                        </v-card-text>
                    </v-card>
                    </v-hover>
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
                height : 'height:520px'

            },
            {
                warna : 'green',
                title : 'Frondend',
                card : [
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                ],
                height : 'height:510px'
        
            },
        ]
        }
    },
}
</script>

<style scoped>
.show-btns {
  color: rgb(0, 255, 234) !important;
}

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
  background: rgb(0, 1, 78); 
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: black; 
}
</style>