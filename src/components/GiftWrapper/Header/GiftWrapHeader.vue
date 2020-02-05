<template>
    <div>
            <v-container>
                <v-row justify="center" align="center" >
                    <v-col>
                    <v-breadcrumbs align-center :items='sections'></v-breadcrumbs>
                    </v-col>
                </v-row>
                <v-row>
                    <v-col>
                        <component :is=selectedSection></component>
                        
                    </v-col>
                </v-row>
            </v-container>
    </div>
</template>

<script lang="ts">
    import Vue from "vue";
    import PointsList from '../Points/PointsList.vue'

    export default Vue.extend({
        components:{
            PointsList:PointsList
        },
        data(){
            return{
                selectedSection:"PointsList",
                sections:[
                    {
                        text:"Points",
                        disabled:false,
                        href:"Points"
                    },
                     {
                        text:"Culling",
                        disabled:false,
                        href:"Culling"
                    },
                     {
                        text:"Methods",
                        disabled:false,
                        href:"Methods"
                    },
                     {
                        text:"Configuration",
                        disabled:false,
                        href:"Configuration"
                    },
                     {
                        text:"Testing",
                        disabled:false,
                        href:"Testing"
                    },
                     {
                        text:"Results",
                        disabled:false,
                        href:"Results"
                    }
                    ]

            }
        }
    });
</script>

<style scoped>

</style>