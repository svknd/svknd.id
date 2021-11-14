<template>
    <v-container
    fluid>
        <br><br>
        <v-container class="teal darken-4 " style="border-radius:20px;">
            <h1 class="text-center white--text">Open Positions</h1>

        <v-container 
        class="teal darken-4 my-5 py-10 con overflow-x-auto scroll hidden-md-and-down"
        >
            <div
            v-for= "n in 5"
            :key= "n"
            class="pb-5 pr-5"
            >
                    <v-container class="bungkus teal accent-4">
                        <v-card class="card teal accent-1">

                        </v-card>
                    </v-container>
            </div>
        </v-container>

        <div class="hidden-xs-and-up">
            <v-row>
                <v-col cols="12" class="pa-0 pt-5">
                    <div>
                        
                    </div>
                </v-col>
            </v-row>
        </div>


        </v-container>
        <br><br>
        <v-container class="grey darken-1 con1" fluid>
            <v-row justify="center">
                <v-col cols="auto">
                   <h1 class="white--text text-center">Join Us</h1>
                </v-col>
            </v-row>
            <v-row align="end">
                <v-col cols="4">
                    <v-img src="/joinus.svg" class="image"></v-img>
                </v-col>
                <v-col cols="8">
                    <v-text-field
                        label="Nama"
                        placeholder="Masukan Nama"
                    ></v-text-field>
                    <v-text-field
                        label="Alamat"
                        placeholder="Masukan Alamat"
                    ></v-text-field>
                    <v-text-field
                        label="Posisi"
                        placeholder="Masukan Posisi"
                    ></v-text-field>
                    <v-text-field
                        label="Kontak"
                        placeholder="Masukan Kontak"
                    ></v-text-field>
                    <v-row justify="start">
                        <v-col cols="auto">
                            <v-btn
                            class="pa-0"
                            depressed
                            color="error"
                            >Batal</v-btn>
                        </v-col>
                        <v-col cols="auto">
                            <v-btn
                            class="pa-0"
                            depressed
                            color="primary"
                            >Kirim</v-btn>
                        </v-col>
                    </v-row>
                </v-col>
            </v-row>
        </v-container>
    </v-container>
</template>

<script>
export default {
    data(){

    }
}
</script>

<style scoped>

.bungkus {
    height: auto;
    width: 1000px;
    border-radius: 10px;
}

.con {
    border-radius: 10px;
    height: 525px;
}

.con1 {
    border-radius: 10px;
    height: 425px;
    width: 1000px;
}

.con2 {
    height: 475px;
    width: 200px;
    background-color: white;
}

.card {
    height: 125px;
    width: 1000px;
}

.title {
 color: white;   
}

.image {
    height: 300px;
    width: 500px;
}

/* width */
::-webkit-scrollbar {
  width: 20px;
}

/* Track */
::-webkit-scrollbar-track {
  box-shadow: inset 0 0 5px grey; 
  border-radius: 10px;
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: red; 
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #b30000; 
}
</style>