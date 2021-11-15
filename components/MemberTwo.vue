<template>
    <div class="member" id="member">
        <v-container>
            <v-row justify="center" class="text-member">
                    <v-col lg="8" md="10" sm="12">
                        <h1>Member</h1>
                        <p>Berikut adalah member yang saat ini masih aktif.</p>
                    </v-col>
            </v-row>
            <v-row>
                <v-col v-for="mem in members" :key="mem" lg="4" md="4" sm="10">
                    <v-card outlined class="card">
                        <img :src="mem.gambar + '.jpg'" alt="" class="pp-member" >
                        <v-row justify="center" class="name-posisi">
                            <div class=" text-center">
                            <span class="hd">{{mem.nama}}</span>
                            <p>{{mem.posisi}}</p>
                        </div>  
                        </v-row>
                    </v-card>
                </v-col>
            </v-row>
        </v-container>  
    </div>
</template>

<script>
export default {
    data() {
    return {
        members:[
            {
                gambar:'orang-2',
                nama : 'Rifki Ahmad Maulana',
                posisi : 'Backend Web Developer'
            },
            {
                gambar:'orang-1',
                nama : 'Raffa Ardiyansah',
                posisi : 'Frontend Web Developer'
            },
            {
                gambar:'orang-3',
                nama : 'Idzhar Maulana',
                posisi : 'QA Engineer'
            }
        ]
    }
    },
}
</script>