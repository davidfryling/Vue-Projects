<template>
    <div v-bind:class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>
            {{ task.text }}
            <span class="fas" >&#10005;</span>
        </h3>
        <p>{{ task.day }}</p>
    </div>
</template>

<script>
export default {
    name: 'Task',
    props: {
        task: Object
    }
}
</script>

<style scoped>
    .reminder {
        border-left: 3px solid green;
    }
    .fas {
        margin-left: 30px; 
        color: red;
    }
</style>