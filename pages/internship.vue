<template>

    <v-container class="grey darken-3" style="height:600px" fluid>
        <v-container class="black" style="height:550px" >

            <v-row class="text-center">
                <v-col class="my-5" >
                    <h1 class="white--text" >Internship</h1>
                </v-col>
            </v-row>

            <v-row
            v-for= "(part, n) in parts"
            :key= "n"
            class="mx-10 overflow-x-auto flex-nowrap" 
            :justify= "part.justify"
            >

                <v-col
                v-for= "n in part.card"
                :key= "n" 
                cols="auto" 
                >
                    <v-card 
                    height="375px" 
                    width="220px"    
                    >
                        <v-img src="https://via.placeholder.com/120x160"></v-img>
                    </v-card>

                </v-col>
            </v-row>

        </v-container>
    </v-container>

</template>

<script>
export default {
    data(){
        return{
            parts : [
                {
                card : 4,
                justify : 'center'
            },
            ]
        }
    }
}
</script>

<style scoped>

</style>