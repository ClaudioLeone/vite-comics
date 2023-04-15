<script>
    export default {
        name: 'AppCta',
        props: {
            src: String,
            img: String,
            title: String
        },
        data() {
            return {
                
            }
        }
    }
</script>

<template>
    <div class="merch-card flex">
        <img :src="src" :alt="img">
        <h4><strong>{{ title }}</strong></h4>
    </div>
</template>

<style scoped lang="scss">
@use "../style/style.scss" as *;

.flex {
    display: flex;
}

.merch-card {
    width: calc(100% / 6 - 5px);
    color: white;
    align-items: center;
    justify-content: space-between;
    cursor: pointer;
}
.merch-card > img {
    width: 40%;
    height: 50px;
}

.merch-card > h4 {
    font-size: 0.6rem;
    padding-left: 5px;
}
</style>