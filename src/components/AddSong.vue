<template>
    <div>
        <form @submit="AddSong">
            <input type="text" v-model="title" name="title" placeholder="Add Song">
            <input type="submit" value="submit" class="btn">
            </form>
        </div>
</template>

<script>
import uuid from "uuid";
export default {
    name: "AddSong",
    data() {
        return {
            title: ''
        }
    },
    methods: {
        AddSong() {
            const newSong = {
                id: uuid.v4(),
                title: this.title,
                completed: false
            }
        }
    }
}
</script>

<style scoped>
form {
    display: flex;
}

input[type="text"] {
    flex: 10;
    padding: 5px;
}

input[type="submit"] {
    flex: 2;
}
</style>