<template>
  <div>
    <select
        name="music_genre" id="music_genre"
        @change="$emit('SelectGenre', selected)"
        v-model='selected'>

        <option value="All">All</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
    </select>
  </div>
</template>

<script>
export default {
    name: "MySearch",
    data(){
        return{
            selected:'All'
        }
    }

}
</script>

<style>

</style>