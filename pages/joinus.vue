<template>

     <!-- <v-expansion-panels>
    <v-expansion-panel
      v-for="(item,i) in 5"
      :key="i"
    >
      <v-expansion-panel-header>
        Item
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels> -->

    <!-- Formulir -->
    <v-container class="grey darken-1 con1 my-10" fluid>
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
        <!-- Akhir dari form -->

</template>    

<script>
export default {
    data(){
        return {
                
        }   
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
    border: 5px solid black;
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