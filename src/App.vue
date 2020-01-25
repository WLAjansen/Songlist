<template>
  <div id="app">
    <Songs v-bind:songs="songs" />
  </div>
</template>

<script>
import Songs from './components/Songs';

export default {
  name: 'app',
  components: {
    Songs
  },
  data() {
    return {
      songs: [
       {
         id: 1,
         title: "Song one",
         completed: false
       },
       {
         id: 2,
         title: "Song two",
         completed: true
       },
       {
         id: 3,
         title: "Song three",
         completed: false
       }
      ]
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Montserrat:400,500,700&display=swap');

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Montserrat;
  line-height: 1.4;
}
</style>
