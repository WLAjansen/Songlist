<template>
    <div>
        <form @submit="addSong">
            <input type="text" v-model="title" name="title" placeholder="Add Song">
            <input type="submit" value="Submit" class="btn">
            </form>
        </div>
</template>

<script>
import uuid from 'uuid';
export default {
    name: "AddSong",
    data() {
        return {
            title: ''
        }
    },
    methods: {
        addSong(e) {
            e.preventDefault();
            const newSong = {
                id: uuid.v4(),
                title: this.title,
                completed: false
            }
            // Send up to parent 
            this.$emit('add-song', newSong);

            this.title = '';
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