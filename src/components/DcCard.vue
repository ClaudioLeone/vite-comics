<script>
    export default {
        name: "DcCard",
        props: {
            thumb: String,
            price: String,
            series: String,
            type: String
        }
    }
</script>

<template>
    <div class="card">
        <img :src="thumb" alt="">
        <h3>{{ series }}</h3>
    </div>
</template>

<style scoped lang="scss">
    .card {
        display: inline-block;
        width: calc((100% / 6) - 10px);
        padding: 5px;
        border: 1px solid black
    }

    h3 {
        font-size: 0.85rem;
        color: white;
        margin-top: 5px;
    }
</style>