<template>
  <div class="single-card">
    <div>immagine</div>
    <div class="info">
        <div class="title">TITOLO</div>
        <div class="author">Aut Tore</div>
        <div class="year">1988</div>

    </div>
  </div>
</template>

<script>
export default {

}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../style/variables';

    .single-card{
        background-color: $secondary_color;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        padding: 15px;
        width: 130px;
        height: 220px;

        

        .info{
            text-align: center;
            border: 1px solid red;
            height: 50%;
            width: 100%;
            color: grey;
            font-size:13px;

            .title{
                font-size: 15px;
                font-weight: 700;
                color: white;
                margin-bottom: 15px;
            }
        }
    }
</style>
