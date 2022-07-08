<template>
    <div class="card-wrapper">
        <div class="single-card">

        <div>
            <img :src="cardDetails.poster" alt="">
        </div>

        <div class="info">
            <div class="title">{{cardDetails.title}}</div>
            <div class="author">{{cardDetails.author}}</div>
            <div class="year">{{cardDetails.year}}</div>

        </div>
  </div>

    </div>
</template>

<script>
export default {
    name: 'MyCard',
    props:{
        cardDetails: Object,

    },

}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    @import '../style/variables';

    .card-wrapper{
        width: calc((100% / 5) - 20px);
        margin: 10px;

        .single-card{
            background-color: $secondary_color;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            padding: 12px;
            width: 130px;
            height: 240px;

            .info{
                text-align: center;
                height: 50%;
                width: 100%;
                color: grey;
                font-size:13px;
                padding-top: 10px;

                .title{
                    font-size: 14px;
                    font-weight: 700;
                    color: white;
                    margin-bottom: 10px;
                    text-transform: uppercase;

                }
            }
        }
    }
</style>
