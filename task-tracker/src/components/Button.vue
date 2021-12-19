<template>
    <button class="btn" v-on:click="$emit('btn-click')" v-bind:style="{background: color }">{{ text }}</button>
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