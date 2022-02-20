<template>
    <v-card style="height : 400px; width: 500px;">
        <v-img :src="currentRestaurant.url"></v-img>
        <h2>{{currentRestaurant.title}}</h2>
        <h4>{{currentRestaurant.type}}</h4>
        <h5>{{currentRestaurant.priceLevel}}</h5>
        
    </v-card>
</template>

<script>
export default {
    props : {
        res : {
            type : Object,
            default () {
                return {
                    title : '',
                    type : '',
                    priceLevel : '$',
                    url : ''
                }
            }
        }
    },
    data () {
        return {
            currentRestaurant : {}
        }
    },
    created () {
        this.currentRestaurant = {...this.res};

    },
    watch : {
        res(value) {
            this.currentRestaurant = value;
        }
    },
    methods :{
        //Fonctions
    }

}
</script>

<style>

</style>