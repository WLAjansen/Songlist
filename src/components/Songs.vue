<template>
  <div>
      <div v-bind:key="song.id" v-for="song in songs">
          <SongItem v-bind:song="song" v-on:del-song="$emit('del-song', song.id)"/>
          </div>
      </div>
</template>

<script>
import SongItem from './SongItem.vue';

export default {
    name: "Songs",
    components: {
        SongItem
    },
    props: ["songs"]
}
</script>

<style scoped>

</style>