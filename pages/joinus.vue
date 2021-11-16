<template>
    <!-- Formulir -->
    <v-main class="pt-0">
    <v-container >
    <v-row 
    style=""
    justify="center"
    >
        <v-col cols="auto" align-self="center">
            <v-text class="font-weight-bold text-h5 text-sm-h4 text-md-h3">
                <font class="title1">MEMBUKA LOWONGAN</font>
                <br>
                <font class="title2">KERJA</font>
            </v-text>
            <br>
        </v-col>
         <v-col align-self="center">
             <v-row justify="center">
                 <v-col cols="auto">
                     <v-img src="join.svg" max-width=""></v-img>
                 </v-col>
             </v-row>
        </v-col>
    </v-row>
    </v-container>


    <v-container
    class="con1"
    >
    <v-container 
    style="height:600px"
    class="black overflow-y-auto flex-nowrap pb-5"> 
        <v-card 
        v-for= "(part, i) in parts"
        :key= "i"
        class= "con"
        >
            <v-card-title class="text-center">
                <v-text class="h6">{{part.title}}</v-text>
            </v-card-title>
            <hr>
            <v-card-text>
                <v-text class="subtitle-1">
                    {{part.content}}
                </v-text>
            </v-card-text>
        </v-card>
    </v-container>
    </v-container>
    
    <v-container class="my-10 con1" >
            <v-row justify="center">
                <v-col cols="auto">
                   <v-text class="white--text text-center text-h3 font-weight-bold">JOIN US</v-text>
                </v-col>
            </v-row>
            <v-row align="end">
                <v-col cols="4">
                    <v-img src="/lowongan.svg" class="image"></v-img>
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
        </v-main>
        <!-- Akhir dari form -->

</template>    

<script>
export default {
    data(){
        return {
            parts : [
                {
                    title : 'Frontend Developer',
                    content : 'Mengembangkan fitur web interface baru untuk pengguna, membuat kode yang reusable ,Menjamin kelayakan teknis dari desain UI/UX, Menjamin semua input pengguna divalidasi dikirim  ke back-end.'
                },
                {
                    title : 'Frontend Developer',
                    content : 'Mengembangkan fitur web interface baru untuk pengguna, membuat kode yang reusable ,Menjamin kelayakan teknis dari desain UI/UX, Menjamin semua input pengguna divalidasi dikirim  ke back-end.'
                },
                {
                    title : 'Frontend Developer',
                    content : 'Mengembangkan fitur web interface baru untuk pengguna, membuat kode yang reusable ,Menjamin kelayakan teknis dari desain UI/UX, Menjamin semua input pengguna divalidasi dikirim  ke back-end.'
                },
                {
                    title : 'Frontend Developer',
                    content : 'Mengembangkan fitur web interface baru untuk pengguna, membuat kode yang reusable ,Menjamin kelayakan teknis dari desain UI/UX, Menjamin semua input pengguna divalidasi dikirim  ke back-end.'
                },
            ]
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
    border: 2px solid black;
}

.con1 {
    background-color: #3F3D56;
    border-radius: 10px;
}

.card {
    height: 125px;
    width: 1000px;
}

.title1 {
    color: rgb(0, 102, 77);   
}
.title2{
    color: rgb(143, 69, 0);
}

.image {
    height: 350px;
    width: 500px;
}

/* width */
::-webkit-scrollbar {
  width: 10px;
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
  background: blueviolet; 
}
</style>