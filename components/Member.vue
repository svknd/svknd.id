<template>
    <div class="member" id="member">
        <v-container>
            <v-row justify="center" class="text-member">
                    <v-col lg="8" md="10" sm="12">
                        <h1>Member</h1>
                        <p>Berikut adalah member yang saat ini masih aktif.</p>
                    </v-col>
            </v-row>
            <v-row justify="center">
                <v-col lg="12" md="12" sm="10">
<v-sheet
    class="mx-auto bungkus-gallery"
    width="100%"
  >
    <v-slide-group
      v-model="model"
      class="pa-1"
      active-class="success"
      show-arrows
    >
      <v-slide-item
        v-for="mem in members" 
        :key="mem"
        v-slot="{ active, toggle }"
      >
        <v-card
          :color="active ? undefined : '#0E8AA6 lighten-1'"
          class="ma-4 card"
          @click="toggle"
        >
                        <img :src="mem.gambar + '.jpg'" alt="" class="pp-member" >
                        <v-row justify="center" class="name-posisi">
                            <div class=" text-center">
                            <span class="hd">{{mem.nama}}</span>
                            <p>{{mem.posisi}}</p>
                        </div>  
                        </v-row>
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
          </v-row>
        </v-card>
      </v-slide-item>
    </v-slide-group>
  </v-sheet>
                </v-col>
            </v-row>
        </v-container>  
    </div>
</template>
                    <!-- <v-card outlined class="card">
                        <img :src="mem.gambar + '.jpg'" alt="" class="pp-member" >
                        <v-row justify="center" class="name-posisi">
                            <div class=" text-center">
                            <span class="hd">{{mem.nama}}</span>
                            <p>{{mem.posisi}}</p>
                        </div>  
                        </v-row>
                    </v-card> -->

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
            },
            {
                gambar:'orang-1',
                nama : 'Ibrahim',
                posisi : 'Qa Engineer'
            },
            {
                gambar:'orang-2',
                nama : 'Irah',
                posisi : 'Mobile Dev'
            },
            {
                gambar:'orang-3',
                nama : 'Pamialhm',
                posisi : 'QA Engineer'
            },
        ]
    }
    },
}
</script>