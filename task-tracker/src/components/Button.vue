<template>
    <button class="btn" v-on:click="$emit('toggle-add-task')" v-bind:style="{background: color }">{{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String
    }
}
</script>