<template>
    <header>
        <div>
            <h1>{{ title }}</h1>
        </div>
        <div class="btn-wrapper">
            <Button v-show="homePage" v-on:btn-click="$emit('toggle-add-task')" class="add-btn" v-bind:text="showAddTask ? 'Close' : 'Add Task' " v-bind:color="showAddTask ? 'red' : 'green' " />
        </div>
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
    },
    computed: {
        homePage() {
            if(this.$route.path === '/') {
                return true;
            } else {
                return false;
            }
        }
    }
}
</script>

<style scoped>
    header {
        /* display: flex;
        justify-content: space-between;
        align-items: center; */
        margin-bottom: 20px;
    }

    h1,
    .btn-wrapper {
        text-align: center;
        margin-bottom: 20px;
    }
</style>
