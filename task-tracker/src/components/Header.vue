<template>
    <header>
        <h1>{{ title }}</h1>
        <Button class="add-btn" text="Add Task" color="green" />
    </header>
</template>

<script>
import Button from './Button.vue'

export default {
    name: 'Header',
    props: {
        title: String,
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
