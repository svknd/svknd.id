<template>
    <!-- Formulir -->
    <v-main class="green darken-4">

    <v-container class="mb-1">
    <v-row justify="center hidden-sm-and-up text-decoration-underline">
        <v-col cols="auto">
            <v-text class="text-subtitle-1 font-weight-bold text-decoration-underline">MEMBUKA LOWONGAN PEKERJAAN!</v-text>
        </v-col>
    </v-row>

    <v-row justify="center hidden-md-and-up hidden-xs-only text-decoration-underline">
        <v-col cols="auto">
            <v-text class="text-h4 font-weight-bold text-decoration-underline">MEMBUKA LOWONGAN PEKERJAAN!</v-text>
        </v-col>
    </v-row>

    <v-row justify="center hidden-sm-and-down">
        <v-col cols="auto">
            <v-text class="text-h3 font-weight-bold text-decoration-underline">MEMBUKA LOWONGAN PEKERJAAN!</v-text>
        </v-col>
    </v-row>
    </v-container>


            <v-container
    class="red"
    >
    <v-container 
    style="height:600px"
    class="black overflow-y-auto flex-nowrap con"> 
        <v-card 
        v-for= "(part, i) in parts"
        :key= "i"
        :class= "part.color"
        class="con">
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
    
    <v-container class="red darken-1 my-10">
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
    border-radius: 10px;
    border: 2px solid black;
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