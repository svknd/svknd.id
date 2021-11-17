<template>
    <div class="joinus" id="joinus">
        <v-container>
            <v-row justify="center" class="text-member">
                    <v-col lg="8" md="10" sm="12">
                        <h1>
                            Join Us
                        </h1>
                    </v-col>
            </v-row>
            <v-row justify="center">
                <v-col lg="8" md="8" sm="12">
                    <v-card class="card">
                        <v-form>
                            <v-text-field
                            label="Nama"
                            required
                            ></v-text-field>
                            <v-select
                            v-model="select"
                            :items="items"
                            :rules="[v => !!v || 'Item is required']"
                            label="Posisi"
                            required
                            ></v-select>
                            <span class="text-info">
                                Posisi yang kami butuhkan tercantum didalam list.
                            </span>
                            <v-text-field
                            label="Kontak"
                            required
                            ></v-text-field>
                            <v-btn
                                color="success"
                                class="mr-4"
                            >
                            Submit
                            </v-btn>
                        </v-form>
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
            items:[
                'Frontend Web Developer',
                'Backend Web Developer',
                'QA Engineer',
                
            ]
        }
    },
}
</script>