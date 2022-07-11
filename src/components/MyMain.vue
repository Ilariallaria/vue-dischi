<template>
  <main>
    <div class="container">
        
        <h2 v-if="albumList.length<10" class="loading">Loading...</h2>
        <MyCard v-for="album,index in albumList" :key="index" :cardDetails="album"/>
        <div><MySearch @SelectGenre="MusicGenre"/></div>
    </div>

  </main>
</template>

<script>

import MyCard from './MyCard.vue'
import axios from "axios"
import MySearch from './MySearch.vue'

export default {
    data(){
        
        return{
            albumList:[],
            
        }
    },

    components: {
        MySearch,
        MyCard,
        },

    methods:{
        getApi(){
            axios.get("https://flynn.boolean.careers/exercises/api/array/music")
            .then((response) =>{
                this.albumList=(response.data.response);
            });
        },

        MusicGenre(selected){
            console.log(selected)
        }
    },
    mounted(){
        setTimeout(this.getApi, 3000);
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';

    main{
        height: 800px;
        background-color: $main_color;

        .container{
            width: 60%;
            margin: 0 auto;
            // padding-top: 20px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            align-content: center;
            height: 600px;

            .loading{
                color: white;
                display: block;
                text-align: center;
            }

        }

        
    }

</style>
