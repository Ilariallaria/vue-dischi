<template>
    <header>
        <div>
            <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/19/Spotify_logo_without_text.svg/2048px-Spotify_logo_without_text.svg.png" alt="">
        </div>
    </header>
</template>

<script>
export default {
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';

header{
    height: 50px;
    background-color: $secondary_color;

    div{
        height: 100%;
        padding: 10px 0 0 15px;

        img{
        width: 30px;
        height: 100%px;
    }

    }
}
</style>
