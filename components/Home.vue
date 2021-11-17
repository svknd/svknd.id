<template>
    <div class="home" id="home">
        <v-row>
            <v-col lg="5" md="5" sm="8">
                <div class="welcome">   
                    <div class="slmt">
                        {{smdang}} <div class="svknd">{{svk}} <span style="color:#FE9720;">{{tch}}</span></div>
                    </div>
                </div>
            </v-col>
            <v-col lg="3" sm="4" offset="2">
                <img src="../assets/img/ic-edu.jpg" alt="" class="ic-raksasa">
            </v-col>
            
        </v-row>
    </div>   
</template>

<script>
export default {
    data() {
        return{
            smdang : 'Selamat Datang di',
            svk : 'Savikindo',
            tch : 'Tech.'
        }
    },
}
</script>

<style scoped lang="scss">

</style>