<script>
    export default {
        name: 'AppCta',
        data() {
            return {
                
            }
        }
    }
</script>

<template>
    <div class="jumbo">
        <div class="container"></div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/style.scss" as *;
.jumbo {
    background-color: #0282F9;

    .container {
        @include containerWdt(80%);
        height: 150px;
        margin: 0 auto;
    }
}
</style>