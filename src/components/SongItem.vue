<template>
    <div class="song-item" v-bind:class="{'is-complete':song.completed}">
        <p>
            <input type="checkbox" v-on:change="markComplete">
            {{song.title}}
            <button @click="$emit('del-song', song.id)" class="del">x</button>
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
.song-item {
    background: #f4f4f4;
    padding: 10px;
    border-bottom: 1px #ccc dotted;
}

.is-complete {
    text-decoration: line-through;
}

.del {
    background: #ff0000;
    color: #fff;
    border: none;
    padding: 5px 9px;
    border-radius: 50%;
    cursor: pointer;
    float: right;
}
</style>