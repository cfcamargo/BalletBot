<template>
    <a href="">{{text}}</a>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
    props: {
        text:{
            type:[String, Number],
            require: true
        }
    }
})
</script>

<style scoped>
    a{
        text-decoration: none;
        display: inline-block;
        padding: .5rem 1rem;
        font-family: 'Sarala', sans-serif;
        color: white;
        
    }
</style>