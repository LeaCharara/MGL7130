<template>
    <div>
        <v-text-field :v-model="search"></v-text-field>
        <v-list>
            <v-list-item v-for="restaurant in restaurants" :key="restaurant.title" style="margin-bottom:20px;">
                <Restaurant :res="restaurant"/>
            </v-list-item>
        </v-list>
    </div>
</template>

<script>
// import HelloWorld from './HelloWorld.vue'
// import NavBar from './NavBar.vue'
import Restaurant from './Restaurant.vue'
export default {
    components : {
        // HelloWorld,
        // NavBar,
        Restaurant
    },
    data () {
        return {
            restaurants : [
                {
                    title:"Mcdonald's",
                    type : 'FastFood',
                    priceLevel : '$',
                    url : 'https://www.incimages.com/uploaded_files/image/1920x1080/getty_1187117706_2000133320009280260_423297.jpg'
                },
                {
                    title:"Poke Monster",
                    type : 'Hawaiian',
                    priceLevel : '$$',
                    url : 'https://pokemonster.ca/wp-content/themes/pokemonster/img/First_Image.png',
                },
            ],
            search :'',
        }
    },
    methods : {
        print(){
            console.log('You clicked me')
        }
    },
    watch :{

    }
}
</script>

<style>
</style>