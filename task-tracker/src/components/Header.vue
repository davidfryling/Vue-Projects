<template>
    <header>
        <h1>{{ title }}</h1>
        <Button v-on:toggle-add-task="$emit('toggle-add-task')" class="add-btn" v-bind:text="showAddTask ? 'Close' : 'Add Task' " v-bind:color="showAddTask ? 'darkred' : 'green' " />
    </header>
</template>

<script>
import Button from './Button.vue'

export default {
    name: 'Header',
    props: {
        title: String,
        showAddTask: Boolean
    },
    components: {
        Button
    }
}
</script>

<style scoped>
    header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    }

    h1 {
        margin-left: 10px;
    }
</style>
