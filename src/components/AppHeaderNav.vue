<script>
    export default {
        name: 'AppHeaderNav',
        data() {
            return {
                title: '>>CONTENT GOES HERE<<'
            }
        }
    }
</script>

<template>
    <div class="headerNav">
        <div class="container">
            <h4>{{ title }}</h4>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../style/style.scss" as *;

.headerNav {
    background-color: #1C1C1C;
    .container {
    @include containerWdt(80%);
    @include flex(row, left, center);
    height: 115px;
    margin: 0 auto;
    color: white;
}
}

</style>