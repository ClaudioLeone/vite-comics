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
        <img :src="thumb" :alt="series">
        <div class="flex title-container">
            <h3>{{ series }}</h3>
        </div>
    </div>
</template>

<style scoped lang="scss">

    .flex {
        display:flex;
    }
    .card {
        cursor: pointer;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        width: calc((100% / 6) - 5px);
        padding: 5px;
        margin: 5px 0;
    }
    .card:hover {
        background-color: #0282F9;
    }

    .title-container {
        height: 100%;
        align-items: flex-end;
    }

    h3 {
        height: fit-content;
        font-size: 0.85rem;
        color: white;
        margin-top: 5px;
    }

    @media screen and (max-width: 910px){
        .card {
            width: calc((100% / 4) - 5px);
        }
    }
</style>