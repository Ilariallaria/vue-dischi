<template>
  <main>
    <div class="container">
        
        <h2 v-if="albumList.length<10" class="loading">Loading...</h2>
        <MyCard v-for="album,index in albumFiltered" :key="index" :cardDetails="album"/>
        <div><MySearch @SelectGenre="filterGenre"/></div>
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
            albumFiltered:[],
            
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

        filterGenre(myGenre){
            if (myGenre === 'All'){
                this.albumFiltered = this.albumList
            }
            else{
            this.albumFiltered = this.albumList.filter((elm) => elm.genre.includes(myGenre))
            }
            // console.log(genre)
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
