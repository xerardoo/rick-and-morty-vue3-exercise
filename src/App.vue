<template>
    <div class="container">
        <h1>Rick and Morty</h1>
        <list-characters></list-characters>
    </div>
</template>

<script>
    import ListCharacters from '@/components/ListCharacters'

    export default {
        components: {ListCharacters}
    }
</script>

<style>

    * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
    }

    body {
        background-color: #24282f;
        color: #fff
    }

    h1 {
        margin-bottom: 3rem;
        text-align: center;
    }
    .container {
        width: 980px;
        max-width: 90%;
        margin: 5rem auto;
    }
    img {
        width: 100%;
    }
</style>
