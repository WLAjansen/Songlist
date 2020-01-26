<template>
    <div class="song-item" v-bind:class="{'is-complete':song.completed}">
        <p>
            {{song.id}}
           <span class="space">{{song.description}}</span>  <span>{{song.title}}</span>
            <button @click="$emit('del-song', song.id)" class="del">Play</button>
            </p>
    </div>
</template>

<script>
export default {
    name: "SongItem",
    props: ["song"],
    methods: {
        markComplete() {
            this.song.completed = !this.song.completed;
        }
    }
}
</script>

<style scoped>

.space {

    position: relative;
   left: 47%;
}

p {
    padding: 10px;
}

img {
    width: 50px;
}
.song-item {
    margin-left: 5px;
    background: #333;
    padding: 10px;
    border-bottom: 1px grey solid;
    color: white;
}

.is-complete {
    text-decoration: line-through;
}

.del {
    background: rgb(4, 179, 4);
    color: #fff;
    border: none;
    padding: 5px 9px;
    border-radius: 5%;
    cursor: pointer;
    float: right;
}
</style>
