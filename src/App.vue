<template>
  <div id="app">
    <MyHeader/>

    <MyMain/>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import MyHeader from'./components/MyHeader.vue'
import MyMain from './components/MyMain.vue'

export default {

  name: 'App',
  components: {
    // HelloWorld
    MyHeader,
    MyMain

  }
}
</script>

<style lang="scss">
@import './style/commons'
</style>
