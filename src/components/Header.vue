<script>
    export default {
        name: "Header",
    }
</script>

<template>
    <header>
        <img src="/src/assets/bernese.png" alt="">
        <p>Bernský salašnický pes</p>
    </header>
</template>

<style scoped>
    header {
        width: 100%;
        height: 5rem;


        display: flex;
        flex-direction: row;
        justify-content: start;
        align-items: center;
        gap: 1rem;
    }

    img {
        width: auto;
        height: 100%;
    }

    p {
        font-family: 'Bebas Neue', sans-serif;

        font-size: 2rem;
        font-weight: bold;

        color: #FDC921;
    }
</style>