<template>
    <div class="internship" id="internship">
        <v-container>
            <v-row justify="center" class="text-member">
                    <v-col lg="8" md="10" sm="12">
                        <h1>Internship</h1>
                        <p>Berikut adalah siswa yang pernah melaksanakan Praktik Kerja Lapangan (PKL) .</p>
                    </v-col>
            </v-row>
            <v-row justify="center">
                <v-col v-for="mem in members" :key="mem" lg="5" md="5" sm="10">
                    <v-card outlined class="card">
                        <img :src="mem.gambar + '.jpg'" alt="" class="pp-orang" align="center">
                        <div class="text-orang">
                            <span class="nama">{{mem.nama}}</span><br>
                            <span class="sekolah">{{mem.sekolah}}</span><br>
                            <span class="tahun">{{mem.tahun}}</span>
                        </div>
                    </v-card>
                </v-col>
            </v-row>
            <!-- <v-row justify="center" class="pagination">
                <v-col lg="1" md="1" sm="1">
                    <v-row>
                        <img src="back.png" width="50px" alt="">
                    </v-row>
                </v-col>
                <v-col lg="1" md="1" sm="1">
                    <v-row>
                        <img src="next.png" height="50px" alt="">
                    </v-row>
                </v-col>
            </v-row> -->
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
                sekolah : 'SMKN 13 Bandung',
                tahun : '2021'
            },
            {
                gambar:'orang-1',
                nama : 'Raffa Ardiyansah',
                sekolah : 'SMKN 13 Bandung',
                tahun : '2021'
            },
            {
                gambar:'orang-3',
                nama : 'Idzhar Maulana',
                sekolah : 'SMKN 13 Bandung',
                tahun : '2021'
            },
            {
                gambar:'orang-2',
                nama : 'Bambang Uhuy',
                sekolah : 'SMKN 13 Bandung',
                tahun : '2021'
            }
        ]
    }
    },
}
</script>