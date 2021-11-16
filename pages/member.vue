<template>
    <v-main>
    <v-container class="mb-3">
    <v-row justify="center">
        <v-col cols="auto">
            <v-text class="text-h3 font-weight-bold">
              <font class="title1">TEAM SAVIKINDO</font><font class="title2"> TECH</font> 
            </v-text>
        </v-col>
    </v-row>
    </v-container>

        <div
        align = "center"
        >

        <!-- Meresponsivekan Justify menggunakan cara manual pada ukuran tablet ke bawah -->
        <v-container
        class = "mb-5 table hidden-sm-and-up"
        v-for= "(part, a) in parts"
        :key= "a"
        :class= "part.warna"
        style = "height:auto; border:20px solid black;"
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

        <!-- Meresponsivekan Justify menggunakan cara manual pada ukuran laptop -->
        <v-container
        v-for= "(part, a) in parts"
        :key= "a"
        class="mb-5 hidden-xs-only"
        :class= "part.warna"
        :style= "part.height"
        style = "border-radius:20px"
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
                title : 'BAGIAN ADMINISTRASI',
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
                  height : 'height:520px',
                  color : 'teal darken-4'
    
            },
            {
                warna : 'red',
                title : 'BACKEND',
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
                height : 'height:520px',
                color : 'black'

            },
            {
                warna : 'green',
                title : 'FRONTEND',
                card : [
                    {
                        nama : 'Fadhil Maulana'
                    },
                    {
                        nama : 'Fadhil Maulana'
                    },
                ],
                height : 'height:510px',
                color : 'red'
        
            },
        ]
        }
    },
}
</script>

<style scoped>
.table {
    border : 5px solid black;
    text-shadow: black;
}

.show-btns {
  color: rgb(0, 255, 234) !important;
}

.con {
    border: 5px solid black;
    border-radius: 20px;
}

.card {
    border-top-left-radius : 5px; 
    border-bottom-left-radius : 5px; 
}

.title1 {
    color: rgb(0, 102, 77);   
}
.title2{
    color: rgb(143, 69, 0);
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