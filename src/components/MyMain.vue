<template>
  <main>
    <div class="container">
        <MyCard/>
    </div>

  </main>
</template>

<script>

import MyCard from './MyCard.vue'

export default {
  components: {
    MyCard
    
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
            padding-top: 50px;
            // test
            height: 550px;
            border: 1px solid white;
        }

        
    }

</style>
