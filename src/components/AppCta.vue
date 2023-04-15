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
        <h4>{{ title }}</h4>
    </div>
</template>

<style scoped lang="scss">
@use "../style/style.scss" as *;

.flex {
    display: flex;
}

.merch-card {
    width: calc(100% / 6 - 5px);
    align-items: center;
    justify-content: space-between;
}
.merch-card > img {
    width: 50%;
    height: 60px;
}

.merch-card > h4 {
    font-size: 0.6rem;
    margin-left: 5px;
}
</style>