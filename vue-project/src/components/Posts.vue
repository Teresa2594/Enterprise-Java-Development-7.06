<template>
    <p>{{id}}. Título: {{ ptitle }}, género: {{ genre }}</p>

</template>

<script>

export default {
props: {
    id:Number,
    title:String,
    genre:String,
}
}

</script>

<style>

</style>