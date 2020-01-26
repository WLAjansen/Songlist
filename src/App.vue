<template>
  <div id="app">
    <Header />
    <Songs v-bind:songs="songs" v-on:del-song="deleteSong" />
  </div>
</template>

<script>
import Header from './components/Header';
import Songs from './components/Songs';

export default {
  name: 'app',
  components: {
    Header,
    Songs
  },
  data() {
    return {
      songs: [
       {
         id: 1,
         title: "The box - Roddy Ricch",
         description: "3:16",
         completed: false,
       },
       {
         id: 2,
         title: "Life is good - Future, drake",
         description: "3:56",
         completed: false
       },
       {
         id: 3,
         title: "Lucid dreams - Juice WLRD",
         description: "3:42",
         completed: false
       },
       {
         id: 4,
         title: "Do not disturb - Smokepurpp",
         description: "2:39",
         completed: false
       },
       {
         id: 5,
         title: "Ranada - Youngboy NBA",
         description: "2:55",
         completed: false
       },
       {
         id: 6,
         title: "Close friends - Lil baby",
         description: "3:23",
         completed: false
       },
       {
         id: 7,
         title: "Hope - XXXTENTACION",
         description: "1:50",
         completed: false
       },
       {
         id: 8,
         title: "One take - Lil tjay",
         description: "2:48",
         completed: false
       },
       {
         id: 9,
         title: "XO Tour Llif3 - Lil uzi vert",
         description: "3:02",
         completed: false
       }
      ]
    }
  },
  methods: {
    deleteSong(id) {
      this.songs = this.songs.filter(song => song.id !== id);
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
  background: #333;
}
</style>
